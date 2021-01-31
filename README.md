# SPV wallet

This is a modified bitc wallet https://github.com/bit-c/bitc. Bitc is a thin SPV bitcoin wallet. It is released under MIT license.

#### Dependencies
- cJSON: a C library to parse JSON objects. It's released under MIT license. http://sourceforge.net/projects/cjson/
- libcurl: an http library. It's released under a MIT/X derivate license. http://curl.haxx.se/libcurl/
- LevelDB: Google's key value store, released under the BSD 3-Clause License. https://github.com/google/leveldb
- OpenSSL: crypto library. https://www.openssl.org/

#### Installing and running
```
make clean
make
./bitc
```

#### Modifications
Modifications are as follows:
- Reduced footprint: ~1mb of header files instead of 35mb in the original version
- Watch-only wallet - fetching transactions in the read-only mode based only on the public key without necessety to provide the private key
- Storing OP_RETURN messages - OP_RETURN scripts are stored separately to parse them.
