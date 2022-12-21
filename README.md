# url-builder-rs
A simple URL builder with no dependencies, useful for a drop-in way to build URLs in a safe way no matter the protocol. See [docs.rs](https://docs.rs/url-builder/0.1.0/url_builder/).

## Example

```rust
use url_builder::URLBuilder;

let mut ub = URLBuilder::new();
ub.set_protocol("http")
    .set_host("localhost")
    .set_port(8000)
    .add_param("first", "1")
    .add_param("second", "2")
    .add_param("third", "3");

println!("{}", ub.build());
```
