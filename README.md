# Description

This image contains Lua bundle contains:
 - LuaJIT 2.1 Beta 2 as Lua interpreter.
 - luarocks package manager.

It have also preinstalled following luarocks' libraries:
 - [luafilesystem](https://keplerproject.github.io/luafilesystem/) as dependency for Penlight.
 - [Penlight](http://stevedonovan.github.io/Penlight/api/index.html) "batteries".
 - [Lrexlib](http://rrthomas.github.io/lrexlib/) regex library in PCRE flavour.

Default working folder is `/app/src/`. So you should mount your scripts into this folder.  

**LuaJIT interpreter** was set as image's entrypoint.  
This allows you to lauch your scripts as if LuaJIT was installed into your OS.

# Usage

Launch your scripts as following command:
```bash
docker run --rm -it -v $(pwd):/app/src tarhan/luajit your_script.lua
```
