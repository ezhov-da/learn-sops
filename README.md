# learn-sops

Sops repo [https://github.com/mozilla/sops](https://github.com/mozilla/sops)

Download Sops for Windows [https://github.com/mozilla/sops/releases/download/v3.6.1/sops-v3.6.1.exe](https://github.com/mozilla/sops/releases/download/v3.6.1/sops-v3.6.1.exe)

Download and install GnuPG for Windows [https://www.gnupg.org/ftp/gcrypt/binary/gnupg-w32-2.2.23_20200903.exe](https://www.gnupg.org/ftp/gcrypt/binary/gnupg-w32-2.2.23_20200903.exe)


Generate key
 ```
gpg --gen-key

name: username
email: username@mail.com
passphrase: username
```

Get key from
```
key BA6887C827163B1E marked as ultimately trusted
```

Encrypt
```
.\sops-v3.6.1.exe --encrypt --in-place --pgp BA6887C827163B1E secret.yml
```

Decrypt 
```
.\sops-v3.6.1.exe --decrypt secret.yml > secret-decrypt.yml
```