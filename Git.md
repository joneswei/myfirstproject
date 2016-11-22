Windows 平台上還有一件要注意的事情，就是對於換行字元的處理與 Unix/Mac 平台不同，會讓 Git 誤判成有修改，因此需要多以下設定：

 > $ git config --global core.autocrlf true
 
 > $ git config --global core.safecrlf true


