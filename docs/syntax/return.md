# Returning values

We promise, this is going to be short!

Returning values is done through the
`return` keyword:

``` bash
return "hello world"
```

Note that functions allow implicit returns,
so you don't need to explicitely use a `return`:

``` bash
func = f(x) {
    x + 1
}

func(9) # 10
```

The default value of a `return` is `null`:

```
if x {
    return; # null
}
```

Please note that **`return` statements without a value
need to include a semicolon**, otherwise the ABS interpreter
will error out, or try to parse the next line as a return
value:

```
fn = f() {
    return
}

fn() # parser errors: no prefix parse function for '}' found

# If the next line contains a parseable value,
# ABS will use that as a return value

fn = f() {
    return
    1
}

fn() # 1
```

## Next

That's about it for this section!

You can now head over to read about [if expressions](/syntax/if).