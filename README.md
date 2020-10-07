[![Workflow Status](https://github.com/enarx/signrel/workflows/test/badge.svg)](https://github.com/enarx/signrel/actions?query=workflow%3A%22test%22)
[![Average time to resolve an issue](https://isitmaintained.com/badge/resolution/enarx/signrel.svg)](https://isitmaintained.com/project/enarx/signrel "Average time to resolve an issue")
[![Percentage of issues still open](https://isitmaintained.com/badge/open/enarx/signrel.svg)](https://isitmaintained.com/project/enarx/signrel "Percentage of issues still open")
![Maintenance](https://img.shields.io/badge/maintenance-activly--developed-brightgreen.svg)

# signrel

This crate provides the `SignRel` trait which maps relationships between
integers that only differ by signedness. For example, both `a` and `b` in
this example have the type `usize`:

```rust
use signrel::SignRel;

let a: <isize as SignRel>::Unsigned = 17;
let b: <usize as SignRel>::Unsigned = 17;

assert_eq!(17usize, a);
assert_eq!(17usize, b);
```

License: Apache-2.0
