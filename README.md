Role Name
=========

fetch Emscripten from github, build and install

Requirements
------------

compilers which is required by Emscripten itself
please see below
https://kripken.github.io/emscripten-site/docs/getting_started/downloads.html#platform-notes-installation-instructions-sdk

Role Variables
--------------

emscripten\_path: path to install default value is "/tmp/emsdk"
emscripten\_version: version identifier default value is "latest"

Dependencies
------------

nothing for now.

Example Playbook
----------------

```
- hosts: all
  become: no

  roles:
    - emscripten
    emscripten_path: "/tmp/emsdk"
    emscripten_version: "latest"
```

please note, become should be changed depending on your package manager
If you are useing homebrew on Mac, it should be no. But it should be yes if you are using Linux package manager (e.g. yum, apt)

License
-------

MIT

Author Information
------------------

Naoyuki Sogo (sogo@longtail-software.co.jp)
