# hushmesh-webpki-roots-pem
This is a crate containing Mozilla's root certificates in PEM format.
This crate is a derived work of [webpki-roots](https://github.com/rustls/webpki-roots).

This crate is inspired by [certifi.io](https://certifi.io/en/latest/) and
uses the data provided by the [Common CA Database (CCADB)](https://www.ccadb.org/).

# License
The underlying data is MPL-licensed, and `src/lib.rs`
is therefore a derived work.

# Regenerating sources
Sources are generated in an integration test, in `tests/codegen.rs`. The test
will fail if the sources are out of date relative to upstream, and update
`src/lib.rs` if so. The code is generated in deterministic order so changes
to the source should only result from upstream changes.
