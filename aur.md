To publish a package to AUR, do the following
1. Config `ssh key` for aur:
```
~/.ssh/config
----------------------
Host aur.archlinux.org
  IdentityFile ~/.ssh/aur
  User aur    
```
*Note*: User is `aur` **not** your username.

2. Generate key with
```
$ ssh-keygen -f ~/.ssh/aur
```     
This will also generate the file `~/.ssh/aur.pub`. Update the `ssh-key` in your account with the content of this file.

3. Create a new repository by cloning an empty repository from AUR
```
$ git clone ssh://aur@aur.archlinux.org/package_name.git
```
For example, for my `rseye-git` package, I will do `$ git clone ssh://aur@aur.archlinux.org/rseye-git.git`

4. Create a new PKGBUILD file.
5. Then run
```
$ makepkg --printsrcinfo > .SRCINFO
$ git add PKGBUILD
$ git add .SRCINFO
$ git commit -a -m "Initial commit"
$ git push
```
6. You just published your package to AUR.

      
       
