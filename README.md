# CryptoDataStore

Choosing a crypto algorithm, choose your key file (something you have) and potentially an extra code/password (something you know) to encrypt the container you wish to secure.
The responsibility of the algorythm to use, the key file, and code/password lies entirely with the user. The user should therefore keep a ledger for these, which should kept. To have a completely automated system the ledger that is owned by the user, like a little black book with links to blobs online/offline, links to the keys in use and having an indicator to teh code/key for each. The idea is never to re-use a key, code/password on any other file, so keeping track is important.

## Validation of correctness

The CryptoDataStore will fail entirely if stored over time and some bytes have gone missing. The concept is to have Forward Error Correction as erasure security using error correction data. See the [WikiPedia - PAR](https://en.wikipedia.org/wiki/Parchive) for the principles of the encrypted data storage. This data could be stored in a ledger (your own) and the un-encrypted files can have a data set like this to be able to ***recover*** segments of original files missing. The encrypted container also needs to have this to be able to proove the decrypted container is as it was supposed to be.

## References

Reed-Solomon Specification: http://web.eecs.utk.edu/~jplank/plank/papers/CS-03-504.html
Reed-Solomon Fault tolerant raid systems: http://web.eecs.utk.edu/~jplank/plank/papers/SPE-9-97.html
Parity Volume Set Specification: https://parchive.sourceforge.net/docs/specifications/parity-volume-spec/article-spec.html
Parity Volume Set version 3 Specification: https://parchive.github.io/doc/Parity_Volume_Set_Specification_v3.0.html
