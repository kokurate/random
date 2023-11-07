            ; DATA XREF from entry0 @ 0x4003fd
┌ 229: int main (int argc, char **argv, char **envp);
│           ; var int64_t var_1b4h @ rbp-0x1b4
│           ; var int64_t var_1b0h @ rbp-0x1b0
│           ; var int64_t var_1afh @ rbp-0x1af
│           ; var int64_t var_1aeh @ rbp-0x1ae
│           ; var int64_t var_1adh @ rbp-0x1ad
│           ; var int64_t var_1ach @ rbp-0x1ac
│           ; var int64_t var_1abh @ rbp-0x1ab
│           ; var int64_t var_1aah @ rbp-0x1aa
│           ; var int64_t var_1a9h @ rbp-0x1a9
│           ; var int64_t var_1a8h @ rbp-0x1a8
│           ; var int64_t var_1a7h @ rbp-0x1a7
│           ; var int64_t var_1a6h @ rbp-0x1a6
│           ; var int64_t var_1a5h @ rbp-0x1a5
│           ; var int64_t var_1a4h @ rbp-0x1a4
│           ; var int64_t var_1a3h @ rbp-0x1a3
│           ; var int64_t var_1a2h @ rbp-0x1a2
│           ; var int64_t var_1a1h @ rbp-0x1a1
│           ; var int64_t var_1a0h @ rbp-0x1a0
│           ; var int64_t var_19fh @ rbp-0x19f
│           ; var int64_t var_19eh @ rbp-0x19e
│           ; var int64_t var_19dh @ rbp-0x19d
│           ; var int64_t var_19ch @ rbp-0x19c
│           ; var int64_t var_19bh @ rbp-0x19b
│           ; var int64_t var_19ah @ rbp-0x19a
│           ; var int64_t var_199h @ rbp-0x199
│           ; var int64_t var_198h @ rbp-0x198
│           ; var int64_t var_4h @ rbp-0x4
│           0x004004d0      55             push rbp
│           0x004004d1      4889e5         mov rbp, rsp
│           0x004004d4      4881ecc00100.  sub rsp, 0x1c0
│           0x004004db      48bf44064000.  movabs rdi, str.Nothing_to_see_here...._n ; 0x400644 ; "Nothing to see here....\n" ; const char *format
│           0x004004e5      c745fc000000.  mov dword [var_4h], 0
│           0x004004ec      c68560feffff.  mov byte [var_1a0h], 0x67   ; 'g' ; 103
│           0x004004f3      c68557feffff.  mov byte [var_1a9h], 0x61   ; 'a' ; 97
│           0x004004fa      c6855dfeffff.  mov byte [var_1a3h], 0x72   ; 'r' ; 114
│           0x00400501      c6855efeffff.  mov byte [var_1a2h], 0x69   ; 'i' ; 105
│           0x00400508      c6855ffeffff.  mov byte [var_1a1h], 0x6e   ; 'n' ; 110
│           0x0040050f      c68555feffff.  mov byte [var_1abh], 0x73   ; 's' ; 115
│           0x00400516      c68567feffff.  mov byte [var_199h], 0x3e   ; '>' ; 62
│           0x0040051d      c68568feffff.  mov byte [var_198h], 0
│           0x00400524      c68559feffff.  mov byte [var_1a7h], 0x6b   ; 'k' ; 107
│           0x0040052b      c68561feffff.  mov byte [var_19fh], 0x73   ; 's' ; 115
│           0x00400532      c68552feffff.  mov byte [var_1aeh], 0x61   ; 'a' ; 97
│           0x00400539      c68556feffff.  mov byte [var_1aah], 0x54   ; 'T' ; 84
│           0x00400540      c6855afeffff.  mov byte [var_1a6h], 0x5f   ; '_' ; 95
│           0x00400547      c68562feffff.  mov byte [var_19eh], 0x5f   ; '_' ; 95
│           0x0040054e      c68551feffff.  mov byte [var_1afh], 0x6c   ; 'l' ; 108
│           0x00400555      c68550feffff.  mov byte [var_1b0h], 0x66   ; 'f' ; 102
│           0x0040055c      c6855bfeffff.  mov byte [var_1a5h], 0x73   ; 's' ; 115
│           0x00400563      c6855cfeffff.  mov byte [var_1a4h], 0x74   ; 't' ; 116
│           0x0040056a      c68563feffff.  mov byte [var_19dh], 0x4c   ; 'L' ; 76
│           0x00400571      c68558feffff.  mov byte [var_1a8h], 0x43   ; 'C' ; 67
│           0x00400578      c68565feffff.  mov byte [var_19bh], 0x41   ; 'A' ; 65
│           0x0040057f      c68566feffff.  mov byte [var_19ah], 0x4f   ; 'O' ; 79
│           0x00400586      c68553feffff.  mov byte [var_1adh], 0x67   ; 'g' ; 103
│           0x0040058d      c68554feffff.  mov byte [var_1ach], 0x3c   ; '<' ; 60
│           0x00400594      c68564feffff.  mov byte [var_19ch], 0x4d   ; 'M' ; 77
│           0x0040059b      b000           mov al, 0
│           0x0040059d      e82efeffff     call sym.imp.printf         ; int printf(const char *format)
│           0x004005a2      31c9           xor ecx, ecx
│           0x004005a4      89854cfeffff   mov dword [var_1b4h], eax
│           0x004005aa      89c8           mov eax, ecx
│           0x004005ac      4881c4c00100.  add rsp, 0x1c0
│           0x004005b3      5d             pop rbp
└           0x004005b4      c3             ret
