#SSH - Github using Windows

* Generate SSH Key

> $ ssh-keygen -t rsa -C "cbalamanatuic@gmail.com"
> Enter file in which to save the key (/c/Users/Admin01/.ssh/id_rsa):/c/Users/Admin01/.ssh/id_rsa_clydeatuic

* Change to SSH Directory

```shell
$ cd /c/Users/Admin01/.ssh
$ ls
```

* Copy public key

```shell
$ subl .
Open id_rsa_clydeatuic.pub
Copy all content and paste it to your Github Account > Settings > SSH and GPG Keys
```

* Add SSH key to the ssh-agent

```shell
Start the ssh-agent in the background
$ eval $(ssh-agent -s)
Agent pid 59566
$ ssh-add ~/.ssh/id_rsa_clydeatuic
```
