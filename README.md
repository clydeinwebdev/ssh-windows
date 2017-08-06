# SSH - Github using Windows

* Generate SSH Key

```console
$ ssh-keygen -t rsa -C "<youremail>@example.com"
Enter file in which to save the key (/c/Users/<PC Name>/.ssh/id_rsa):/c/Users/<PC Name>/.ssh/id_rsa_<github name>
```

* Change to SSH Directory

```console
$ cd /c/Users/<PC Name>/.ssh
$ ls
```

* Copy public key

```console
$ subl .
Open id_rsa_<github name>.pub
Copy all content and paste it to your Github Account > Settings > SSH and GPG Keys
```

* Add SSH key to the ssh-agent

```console
Start the ssh-agent in the background
$ eval $(ssh-agent -s)
Agent pid 59566
$ ssh-add ~/.ssh/id_rsa_<github name>
```

* Manage multiple accounts

```console
# <github name> Github
Host github-<github name>
	HostName github.com
	User git
	IdentityFile ~/.ssh/id_rsa_<github name>
	
# clydeinwebdev Github
Host github-clydeinwebdev
	HostName github.com
	User git
	IdentityFile ~/.ssh/id_rsa_clydeinwebdev
```
