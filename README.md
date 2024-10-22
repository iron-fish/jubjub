Implementation of the [Jubjub][jubjub] elliptic curve group and its associated
fields.

This is a fork of the original [`jubjub`][jubjub-crate] crate from Zcash. The
fork was created by the Iron Fish project to add performance improvements.

## Delta from upstream

These are the differences between this crate and the upstream
[`jubjub`][jubjub-crate] crate:

* Changed the elliptic curve backend from [`bls12_381`][bls12_381] to
  [`blstrs`][blstrs]
* Added optional statistics counters for performance monitoring. This can be
  enabled through the `stats` feature.
* Added a `ExtendedPoint::multiply_many` method to efficiently perform multiple
  elliptic curve multiplications in one call.
* Added a `SubgroupPoint::as_extended` method to convert a `SubgroupPoint` to
  an `ExtendedPoint`.

[jubjub]: https://zips.z.cash/protocol/protocol.pdf#jubjub
[jubjub-crate]: https://crates.io/crates/jubjub
[bls12_381]: https://crates.io/crates/bls12_381
[blstrs]: https://crates.io/crates/blstrs
