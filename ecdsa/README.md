# RustCrypto: ECDSA

[![crate][crate-image]][crate-link]
[![Docs][docs-image]][docs-link]
![Apache2/MIT licensed][license-image]
![MSRV][rustc-image]
[![Project Chat][chat-image]][chat-link]
[![Build Status][build-image]][build-link]

[Elliptic Curve Digital Signature Algorithm (ECDSA)][1] as specified in
[FIPS 186-4][2] (Digital Signature Standard).

[Documentation][docs-link]

## About

This crate provides generic ECDSA support which can be used in the following
ways:

- Generic implementation of ECDSA usable with the following crates:
  - [`k256`] (secp256k1)
  - [`p256`] (NIST P-256)
- Other crates which provide their own complete implementations of ECDSA can
  also leverage the types from this crate to export ECDSA functionality in a
  generic, interoperable way by leveraging [`ecdsa::Signature`] with the
  [`signature::Signer`] and [`signature::Verifier`] traits.

## Minimum Supported Rust Version

This crate requires **Rust 1.47** at a minimum.

We may change the MSRV in the future, but it will be accompanied by a minor
version bump.

## License

All crates licensed under either of

 * [Apache License, Version 2.0](http://www.apache.org/licenses/LICENSE-2.0)
 * [MIT license](http://opensource.org/licenses/MIT)

at your option.

### Contribution

Unless you explicitly state otherwise, any contribution intentionally submitted
for inclusion in the work by you, as defined in the Apache-2.0 license, shall be
dual licensed as above, without any additional terms or conditions.

[//]: # (badges)

[crate-image]: https://img.shields.io/crates/v/ecdsa.svg
[crate-link]: https://crates.io/crates/ecdsa
[docs-image]: https://docs.rs/ecdsa/badge.svg
[docs-link]: https://docs.rs/ecdsa/
[license-image]: https://img.shields.io/badge/license-Apache2.0/MIT-blue.svg
[rustc-image]: https://img.shields.io/badge/rustc-1.47+-blue.svg
[chat-image]: https://img.shields.io/badge/zulip-join_chat-blue.svg
[chat-link]: https://rustcrypto.zulipchat.com/#narrow/stream/260048-signatures
[build-image]: https://github.com/RustCrypto/signatures/workflows/ecdsa/badge.svg?branch=master&event=push
[build-link]: https://github.com/RustCrypto/signatures/actions?query=workflow%3Aecdsa

[//]: # (footnotes)

[1]: https://en.wikipedia.org/wiki/Elliptic_Curve_Digital_Signature_Algorithm
[2]: https://csrc.nist.gov/publications/detail/fips/186/4/final

[//]: # (docs.rs definitions)

[`ecdsa::Signature`]: https://docs.rs/ecdsa/latest/ecdsa/struct.Signature.html
[`k256`]: https://docs.rs/k256
[`p256`]: https://docs.rs/p256
[`signature::Signer`]: https://docs.rs/signature/latest/signature/trait.Signer.html
[`signature::Verifier`]: https://docs.rs/signature/latest/signature/trait.Verifier.html
