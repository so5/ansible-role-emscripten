Emscripten
=========

fetch Emscripten from github, build and install

Requirements
------------

all required and missing packages will be installed in this role

Role Variables
--------------

```
emscripten_path: path to install default value is "/tmp/emsdk"
emscripten_version: version identifier default value is "latest"
```

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
