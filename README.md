# BlockChain-Go-Wallet
Create And Sign Bitcoin Transactions With Golang

# Create And Sign Bitcoin Transactions With Golang

##### 1 - Bitcoin transactions
A transaction is the mechanism for spending bitcoins. In a transaction, the owner of some bitcoins transfers ownership to a new address.
![alt text](https://cdn-images-1.medium.com/max/1200/0*5KYn60W30-mXorZT.)
##### 2 - Cryptography
Bitcoin uses digital signatures to ensure that only the owner of bitcoins can spend them. The owner of a Bitcoin address has the private key associated with the address. To spend bitcoins, they sign the transaction with this private key, which proves they are the owner. (It's somewhat like signing a physical check to make it valid.) A public key is associated with each Bitcoin address, and anyone can use it to verify the digital signature.
Blocks and transactions are identified by a 256-bit cryptographic hash of their contents. This hash value is used in multiple places in the Bitcoin protocol. In addition, finding a special hash is the difficult task in mining a block.

##### 3 - Bitcoin addresses and keys
Bitcoin uses a variety of keys and addresses, so the following diagram may help explain them. so we start by creating a random 256-bit private key. The private key is needed to sign a transaction and thus transfer (spend) bitcoins. Thus, the private key must be kept secret or else your bitcoins can be stolen.

The Elliptic Curve DSA algorithm generates a 512-bit public key from the private key.  This public key is used to verify the signature on a transaction. Inconveniently, the Bitcoin protocol adds a prefix of 04 to the public key. The public key is not revealed until a transaction is signed, unlike most systems where the public key is made public.

![alt text](https://asecuritysite.com/bithash.png)

The next step is to generate the Bitcoin address that is shared with others. 
The key is then encoded in ASCII using Bitcoin's custom Base58Check encoding. The resulting address, such as '1KKKK6N21XKo48zWKuQKXdvSsCf95ibHFa' , is the address people publish in order to receive bitcoins. Note that you cannot determine the public key or the private key from the address. If you lose your private key (for instance by throwing out your hard drive), your bitcoins are lost forever. 

##### 3 - Wallet import format
A WIF private key is just another way of representing your original private key. If you have a WIF private key, you can always convert it back in to its original format.

This is all then converted to Base58, which shortens the entire thing and makes it easier to transcribe .

![alt text](http://learnmeabitcoin.com/glossary/images/private-key/wif.svg)

The wallet import format is shorter, and includes built-in error checking codes so that typos can be automatically detected and/or corrected (which is impossible in hex format) and type bits indicating how it is intended to be used. Wallet import format is the most common way to represent private keys in Bitcoin.

# Download/Install Packages

```sh
$ mkdir $GOPATH\github.com\btcsuite
$ go get -u github.com/btcsuite/btcutil
$ go get -u github.com/btcsuite/btcd
$ go get -u github.com/btcsuite/btclog
```

# Build Program 

```sh
$ mkdir YourWorkSpace
$ git clone Link.com
$ go build 
$ fileName.exe
```
and then Get the contract info in json file 

```sh
{
  "txid": "4e8378675bcf6a389c8cfe246094aafa44249e48ab88a40e6fda3bf0f44f916a",
  "source_address": "1MMMMSUb1piy2ufrSguNUdFmAcvqrQF8M5",
  "destination_address": "1KKKK6N21XKo48zWKuQKXdvSsCf95ibHFa",
  "amount": 91234,
  "unsignedtx": "0100000001484d40d45b9ea0d652fca8258ab7caa42541eb52975857f96fb50cd732c8b4810000000000ffffffff0162640100000000001976a914df3bd30160e6c6145baaf2c88a8844c13a00d1d588ac00000000",
  "signedtx": "01000000016a914ff4f03bda6f0ea488ab489e2444faaa946024fe8c9c386acf5b6778834e000000008b483045022100904dbeddeecccf6391ac92922381ae006bf244c002f42e195daa0a9837a4b5820220461677f9dbb7d9580e268ac486cfeb4b9d87bfdd6d4e7b1be09b8e6f5cc0a70701410414e301b2328f17442c0b8310d787bf3d8a404cfbd0704f135b6ad4b2d3ee751310f981926e53a6e8c39bd7d3fefd576c543cce493cbac06388f2651d1aacbfcdffffffff0162640100000000001976a914c8e90996c7c6080ee06284600c684ed904d14c5c88ac00000000"
}
```



### Tech

to get deeper knowledge :
Generate Cryptocurrency Private Keys And Public Addresses With Golang  https://www.thepolyglotdeveloper.com/2018/02/generate-cryptocurrency-private-keys-public-addresses-golang/

Bitcoins the hard way
http://www.righto.com/2014/02/bitcoins-hard-way-using-raw-bitcoin.html


Enjoy !
:)




M-AMAIRI


