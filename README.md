# mpy-bitcoin

extends `hashlib` micropython module and adds `_ecc` module with optimized C implementation of elliptic curves and hashing algorithms.

Also contains a single-line pbkdf2_hmac_sha512 algorithm:

`pbkdf2_hmac_sha512(password, salt, iterations, bytes_to_read)`

in Bitcoin to generate a seed:

`pbkdf2_hmac_sha512(mnemonic, 'mnemonic'+password, 2048, 64)`