### fakultas model

```
class fakultas extends Model
{
    use HasFactory;
    
    protected $guarded = ['id'];

    public function jurusan_prodi()
    {
        return $this->hasMany(jurusan_prodi::class);
    }

    public function user(){
        return $this->hasMany(User::class);
    }

}
```

### jurusan_prodi model
```
class jurusan_prodi extends Model
{
    use HasFactory;

    protected $guarded = ['id'];

    public function fakultas()
    {
        return $this->belongsTo(fakultas::class);
    }

    public function user(){
        return $this->hasMany(User::class);
    }
}
```

### user model
class User extends Authenticatable
{
    use HasApiTokens, HasFactory, Notifiable;

    protected $guarded = ['id'];

 
    public function jurusan_prodi()
    {
        return $this->belongsTo(jurusan_prodi::class);
    }

    public function fakultas()
    {
        return $this->belongsTo(fakultas::class);
    }

}

### jurusan_prodi migrations

```
  Schema::create('jurusan_prodis', function (Blueprint $table) {
            $table->id();
            $table->unsignedBigInteger('fakultas_id');
            $table->foreign('fakultas_id')->references('id')->on('fakultas')->onDelete('cascade');        
            $table->string('nama');
            $table->timestamps();
        });
```

### fakultas migrations
```
Schema::create('fakultas', function (Blueprint $table) {
            $table->id();
            $table->string('nama');
            $table->timestamps();
        });
```
### user migration
```
Schema::create('users', function (Blueprint $table) {
            $table->id();
    
            $table->foreignId('fakultas_id')->nullable();
            $table->foreignId('jurusan_prodi_id')->nullable();
      
            $table->rememberToken();
            $table->timestamps();
        });
```

