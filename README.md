Loo
===

[![Build Status](https://travis-ci.org/killdream/loo.png)](https://travis-ci.org/killdream/loo)


Like [Boo][], but for Lua. Loo provides the basic prototypical primitives and
combinators so you can structure your programs easily.

```lua
local loo = require("loo")

local Animal = loo.Base:derive({ name = 'Unknown' })

function Animal:say(thing)
  return self.name .. ": " .. thing
end

local Cat = Animal:derive()

function Cat:_init(name)
  if name then self.name = name end
end

local nyah = Cat:make("Nyan Cat")
nyah:say("Nyan nyan nyan~")
```

### Installing

...


### Testing

Install Busted, then run the specs:

```bash
$ luarocks install busted
$ busted
```

(this assumes you have LuaRocks already installed on your system.)


### Docs & Reference

...


### Licence

MIT/X11.


[Boo]: http://github.com/killdream/Boo
