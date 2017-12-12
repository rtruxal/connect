Connect
=======
[![py2badge](https://img.shields.io/badge/Python-2.7-blue.svg)]

# Before We Begin!
THERE ARE BETTER WAYS TO DO THIS...FOR EXAMPLE JUST EDIT `~/.ssh/config`
Here's a link right [here.](http://nerderati.com/2011/03/17/simplify-your-life-with-an-ssh-config-file/)  



# WHAT IS IT?:
#### It's a replacement for `$ ssh -i <private-keyfile> [username]@<some_host>`
#### Instead just type: `$ connect host_nickname`
#### Also it's a simple ssh-engine...kinda like a reeeeeaaaaly small & crappy version of Ansible made by 1 person.
...
#### USE IT FOR LEARNING!...Like I did!

# DIRECTIONS:
 1.  Modify 2 dictionaries inside the `connect` file. (the `dict`s are called `translator_dict` & `pathdict`)
 2.  Place this file somewhere in your $PATH (Ex: `~/bin/connect` or `/usr/bin/connect`)
 3.  Make it executable (Ex: `chmod u+x ~/bin/connect`)
 4.  from the shell of your choice enter:
 ```sh
     $ connect host1
     Warning: Permanently added the RSA host key for IP address 'xxx.xxx.xxx.xxx'
     to the list of known hosts.
     Enter passphrase for key '/path/to/host1/keyfile.openssh':
 ```

# THE INNARDS:
```py
"""
  - the pathdict variable is important.

  - Here's the format of pathdict:
    - `{'hostname' : ('/path/to/private/key/file.openssh', 'user@www.foo-domain.com')}
         ^--|---^      ^---------------|---------------^    ^-----------|---------^
            |                          |                                |
       the name of the           for ssh's -i                      let's take a
       box to ssh into              option                          wild guess
"""
```

# REQUIREMENTS:
 - A UNIX-based OS. (No Windows unfortunately. `os.execlp()` is the culprit-requirement.)
 - Python 2.7 (Help with supporting python3 is welcome!)

# SALES PITCH:
#### Do you frequently use ssh with the `-i` option & find yourself struggling to remember:
 - /the/path/to/the/right/keyfile.openssh
 - TheRightUserName@the-correct-domain.com
#### Well worry no more! Just:...



#### shizzizam.
fin.
