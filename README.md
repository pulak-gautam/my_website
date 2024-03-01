- To get shell access
    ``ssh -oKexAlgorithms=+diffie-hellman-group1-sha1 -oHostKeyAlgorithms=+ssh-rsa <username>@webhome.cc.iitk.ac.in``
- To open up sftp console
    ``sftp -oKexAlgorithms=diffie-hellman-group-exchange-sha1 -oHostKeyAlgorithms=+ssh-rsa <username>@172.31.1.148``
- To cp/delete files on ftp server. \
    There are multiple ways to do this
    - You may use ``rsync`` to do this
        ``rsync -e 'ssh -oKexAlgorithms=+diffie-hellman-group1-sha1 -oHostKeyAlgorithms=+ssh-rsa' -alPvz <local-folder-path> <username>@webhome.cc.iitk.ac.in:/www/<username>/www/``
    - You may otherwise use ssh commands like ``scp``
    - Or, you may directly open up ftp console and, use ``put`` and ``get``


