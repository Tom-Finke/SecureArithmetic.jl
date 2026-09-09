# Remote Computation with ObliviousOffload.jl

Homomorphic encryption is perfectly suited to process sensitive data on a remote server without
exposing the underlying plaintext. A client encrypts its data locally, sends the ciphertext and public key
to the server, and the server performs computations entirely on encrypted data before
returning the encrypted result. The client can then decrypt the result with its private key.

[ObliviousOffload.jl](https://github.com/hpsc-lab/ObliviousOffload.jl) provides exactly
this client–server workflow on top of SecureArithmetic.jl. It handles TLS-secured HTTP
transport, serialization of SecureArithmetic objects, and a simple
`register_service!` / `offload` API.

For an example of how to use ObliviousOffload.jl, see the provided [simple array operations example](https://github.com/hpsc-lab/ObliviousOffload.jl/tree/main/examples/simple_array_operations) and the
[ObliviousOffload.jl documentation](https://hpsc-lab.github.io/ObliviousOffload.jl/stable).
