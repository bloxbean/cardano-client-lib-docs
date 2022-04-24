# cardano-client-lib

A client library for Cardano in Java. This library simplifies the interaction with Cardano blockchain from a Java application.

**Latest Beta**: [0.2.0-beta3](https://github.com/bloxbean/cardano-client-lib/releases/tag/v0.2.0-beta3) (Pure Java)

**Previous Stable Version** : [0.1.5](https://github.com/bloxbean/cardano-client-lib/releases/tag/v0.1.5) (Uses rust lib)

[v0.1.5 More details](README-0_1_5.md)

**Posts**
- [Cardano-client-lib : A Java Library to interact with Cardano - Part I](https://medium.com/p/83fba0fee537)
- [Cardano-client-lib: Transaction with Metadata in Java - Part II](https://medium.com/p/fa34f403b90e)
- [Cardano-client-lib: Minting a new Native Token in Java - Part III](https://medium.com/p/1a94a21cfeeb)
- [Composable functions to build transactions](https://medium.com/coinmonks/cardano-client-lib-new-composable-functions-to-build-transaction-in-java-part-i-be3a8b4da835)

**Examples**

[Cardano-client-lib examples repository](https://github.com/bloxbean/cardano-client-examples/)

[JavaDoc](https://javadoc.io/doc/com.bloxbean.cardano/cardano-client-lib/0.2.0-beta3/index.html)

**Features**

#### Address Generation

- Address Generation (Base Address, Enterprise Address)
- Generate Address from Mnemonic phase

#### Transaction Serialization & Signing
- API to build Payment transaction (ADA & Native Tokens)
- CBOR serialization of transaction
- Transaction signing

### High Level api
- To build and submit
    -  Payment transaction
    - Token Minting and token transfer transaction

### Composable Functions
- To build and submit
    - Payment transaction
    - Token Minting and token transfer
    - Plutus smart contract call
    - Token minting with Plutus contract

[Examples with Composable Functions](https://github.com/bloxbean/cardano-client-examples/tree/main/src/main/java/com/bloxbean/cardano/client/examples/function)

#### Metadata Builder
- Helper to build Metadata
- Converter to conver JSON (No Schema) to Metadata format

#### Token Minting
- Token Minting transaction builder
- Native script (ScriptAll, ScriptAny, ScriptAtLeast, ScriptPubKey, RequireTimeAfter, RequireTimeBefore)
- Policy Id generation

#### Backend Integration
The library also provides integration with Cardano node through different backend services.
Out of box, the library currently supports integration with following providers through the Backend api.

- [Blockfrost](https://blockfrost.io)
    - **Module :** cardano-client-backend-blockfrost [README](https://github.com/bloxbean/cardano-client-lib/blob/master/backend-modules/blockfrost/README.md)
    - **Status :** Stable
- [Koios](https://www.koios.rest/)
    - **Module :** cardano-client-backend-koios [README](https://github.com/bloxbean/cardano-client-lib/blob/master/backend-modules/koios/README.md)
    - **Status :** Beta
- [Ogmios](https://ogmios.dev/)
    - **Module :** cardano-client-backend-koios [README](https://github.com/bloxbean/cardano-client-lib/blob/master/backend-modules/ogmios/README.md)
    - **Status :** Experimental
    - **Supported Apis :** submitTransaction, evaluateTx
- [cardano-graphql](https://github.com/input-output-hk/cardano-graphql)
    - **Module :** cardano-client-backend-gql [README](https://github.com/bloxbean/cardano-client-lib/blob/master/backend-modules/cardano-graphql/README.md)
    - **Status :** Deprecated

**Following Backend apis are currently available**
- TransactionService (Submit transaction, Get transaction, Evaluate ExUnits for Script Txn)
- AddressService (Get address details)
- UtxoService (Get utxos for an address)
- AssetService
- BlockService
- NetworkInfoService
- EpochService
- MetadataService

