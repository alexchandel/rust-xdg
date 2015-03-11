rust-xdg is a library that makes it easy to follow the standards for directories.

## Usage

```rust
use xdg::XdgDirs;
use std::fs::File;

let dirs = XdgDirs::new();
let data_dir = dirs.want_write_data("AppName");

let mut f = File::create(data_dir.join("data.txt"));
f.write(b"Some data.\n");
```

## License

rust-xdg is primarily distributed under the terms of both the MIT license
and the Apache License (Version 2.0).

See LICENSE-APACHE and LICENSE-MIT for details.
