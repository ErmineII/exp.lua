exp.lua
=======

infix expression evaluator

You will find bugs. If you embed this anywhere it could provide a security
risk (including it's input capability). Bound to break sometime because
it's made with mostly regexs and ugly hacks. Also not finished. With that
aside ...

Usage
-----

```lua
local exp = require 'exp'

-- if you have a custom variable storage mechanism or you want some kind of inter-op
exp.getvariable = smt
exp.setvariable = smtelse

exp.eval '1+1' -- 2
exp.eval 'z=1+2; z?1:2' -- 1, '' and 0 are false
exp.eval 'y=z%2; y+1' -- 1
```
