Connect
=======

#WHAT IS IT?:
####It's a replacement for `$ ssh -i <private-keyfile> [username@[some_host]]`
####Instead just type: `$ connect some_host`

#THE INNARDS:
```py
"""
  - the pathdict variable is important.

  - Here's the format of pathdict:
    - `{'hostname' : ('/path/to/private/key/file.openssh', 'user@www.foo-domain.com')}
         ^--|---^      ^---------------|---------------^    ^-----------|---------^
            |                          |                                |
       the name of the           for ssh's -i                      let's take a
       box to ssh into              option                          wild guess

  - make sure you get these mappings right or nothing will work.
"""
```

#REQUIREMENTS:
 - A UNIX-based OS. (That means Linux & Mac if you're new to computa's)
 - Python 2.7 (Help with supporting python3 is welcome!)

#SALES PITCH:
####Do you frequently use ssh with the `-i` option & find yourself struggling to remember:
 - /the/path/to/the/right/keyfile.openssh
 - TheRightUserName@the-correct-domain.com
####Well worry no more! Just:...

#DIRECTIONS:
 1.  Modify 2 dictionaries inside the script. (They are called `translator_dict` & `pathdict`)
 2.  Place this file somewhere in your $PATH (Ex: `~/bin/connect` or `/usr/bin/connect`)
 3.  Make it executable (Ex: `chmod u+x ~/bin/connect`)
 4.  from the shell of your choice enter:
 ```sh
     $ connect host1
     Warning: Permanently added the RSA host key for IP address 'xxx.xxx.xxx.xxx'
     to the list of known hosts.
     Enter passphrase for key '/path/to/host1/keyfile.openssh':
 ```


 ####shizzizam.  
fin.
