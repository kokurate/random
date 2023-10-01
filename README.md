### Controller
```
    public function update_user(Request $request, $id){
        $validatedData = $request->validate([
            'name' => 'required|max:255',
            'username' => ['required', 'min:3', 'max:255', 'unique:users,username,'.$id],
            'email' => 'required|email:dns|unique:users,email,'.$id,
        ]);

        if($request->password != NULL){
            $validatedData['password'] = bcrypt($request->password);
        }

        User::where('id', $id)->update($validatedData);

        return redirect()->route('user')->with('success','Data Berhasil Di Update!');
    }

```

### view

```
<form action="/update_user/{{ $dataUser->id }}" method="POST" enctype="multipart/form-data">
        @csrf
        <div class="mb-3">
          <label for="name" class="form-label">Nama</label>
          <input type="text" class="form-control" id="name" name="name"
          value="{{ $dataUser->name }}">
          @error('name') <span class="text-danger">{{ $message }}</span>@enderror
        </div>
        <div class="mb-3">
          <label for="username" class="form-label">username</label>
          <input type="text" class="form-control" id="username" name="username"
          value="{{ $dataUser->username }}">
          @error('username') <span class="text-danger">{{ $message }}</span>@enderror

        </div>
        <div class="mb-3">
          <label for="email" class="form-label">Email</label>
          <input type="text" class="form-control" id="email" name="email"
          value="{{ $dataUser->email }}">
          @error('email') <span class="text-danger">{{ $message }}</span>@enderror

        </div>
        <div class="mb-3">
          <label for="password" class="form-label">Password</label>
          <input type="password" class="form-control" id="password" name="password"
          value="">

        </div>
        <button type="submit" class="btn btn-primary">Submit</button>
      </form>
```
