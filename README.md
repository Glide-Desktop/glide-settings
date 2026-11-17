# Glide Settings

The settings app of the [Glide desktop](https://github.com/Glide-Desktop). It
reads and writes the shell's settings through `glide-configd` (from
[glide-shell](https://github.com/Glide-Desktop/glide-shell)) and talks to
NetworkManager, BlueZ, AccountsService, timedate1, locale1 and the other
system services directly.

## Build

```sh
cargo build --release
```

The shared crates come from a tag of
[glide-libs](https://github.com/Glide-Desktop/glide-libs). To build against a
checkout of glide-libs next to this one, create `.cargo/config.toml` (ignored
by git):

```toml
[patch."https://github.com/Glide-Desktop/glide-libs"]
glide-app = { path = "../glide-libs/crates/glide-app" }
glide-config = { path = "../glide-libs/crates/glide-config" }
glide-ipc = { path = "../glide-libs/crates/glide-ipc" }
glide-netbird = { path = "../glide-libs/crates/glide-netbird" }
glide-paint = { path = "../glide-libs/crates/glide-paint" }
glide-sdk = { path = "../glide-libs/crates/glide-sdk" }
glide-theme = { path = "../glide-libs/crates/glide-theme" }
```

Split from the Glide monorepo with its history in November 2026.
