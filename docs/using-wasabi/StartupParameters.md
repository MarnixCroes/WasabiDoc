---
{
  "title": "Starting Wasabi with parameters",
  "description": "A guide on starting Wasabi with parameters, using the command line interface. This is the Wasabi documentation, an archive of knowledge about the open-source, non-custodial and privacy-focused Bitcoin wallet for desktop."
}
---

# Starting Wasabi with parameters

[[toc]]

## Available commands

It is possible to start Wasabi with specific parameters.
The parameters override the configurations in the configuration file.

When entering the commands on the command line, they are capital letter insensitive.

The parameters work for both the GUI and the [Daemon](/using-wasabi/Daemon.md).

> Help about the options is available when using the command line by adding `--help` to the executable: _wassabeed --help_ or _dotnet run -- --help_ when building from source.

### Config file configurations

All configuration options available via the `Config.json` file are also available as command line arguments:

| Config File | Command Line | Environment variable |
|---------|--------|----------------------|
| ""Network": "TestNet" | --network=testnet | WASABI_NETWORK=testnet |
| "MainNetBackendUri": "https://api.wasabiwallet.io/" | --mainnetbackenduri="https://api.wasabiwallet.io/" | WASABI_MAINNETBACKENDURI="https://api.wasabiwallet.io/"|
| "TestNetBackendUri": "https://api.wasabiwallet.co/" | --testnetbackenduri="https://api.wasabiwallet.co/" | WASABI_TESTNETBACKENDURI="https://api.wasabiwallet.co/" |
| "RegTestBackendUri": "http://localhost:37127/" | --regtestbackenduri="http://localhost:37127/" | WASABI_REGTESTBACKENDURI="http://localhost:37127/" |
| "MainNetCoordinatorUri": "" | --mainnetcoordinatoruri="" | WASABI_MAINNETCOORDINATORURI="" |
| "TestNetCoordinatorUri": "https://api.wasabiwallet.co/" | --testnetcoordinatoruri="https://api.wasabiwallet.co/" | WASABI_TESTNETCOORDINATORURI="https://api.wasabiwallet.co/" |
| "RegTestCoordinatorUri": "http://localhost:37128/" | --regtestcoordinatoruri="http://localhost:37128/" | WASABI_REGTESTCOORDINATORURI="http://localhost:37128/" |
| "UseTor": "Enabled" | --usetor=enabled | WASABI_USETOR=enabled |
| "TerminateTorOnExit": false | --terminatetoronexit=false | WASABI_TERMINATETORONEXIT=false |
| "TorBridges": "[TorBridge]" | --torbridges="[TorBridge]" | WASABI_TORBRIDGES="[TorBridge]" |
| "DownloadNewVersion": true | --downloadnewversion=true | WASABI_DOWNLOADNEWVERSION=true |
| "UseBitcoinRpc": true | --usebitcoinrpc=true | WASABI_USEBITCOINRPC=true |
| "BitcoinRpcCredentialString": "rpcuser:rpcpassword" | --bitcoinrpccredentialstring="rpcuser:rpcpassword" | WASABI_BITCOINRPCCREDENTIALSTRING="rpcuser:rpcpassword" |
| "BitcoinRpcEndpoint": "http://127.0.0.1:8333" | --bitcoinrpcendpoint="http://127.0.0.1:8333" | WASABI_BITCOINRPCENDPOINT="http://127.0.0.1:8333" |
| "JsonRpcServerEnabled": true | --jsonrpcserverenabled=true | WASABI_JSONRPCSERVERENABLED=true |
| "JsonRpcUser": "" | --jsonrpcuser="" | WASABI_JSONRPCUSER="" |
| "JsonRpcPassword": "" | --jsonrpcpassword="" | WASABI_JSONRPCPASSWORD="" |
| "JsonRpcServerPrefixes":["http://127.0.0.1:37128/", "http://localhost:37128/"] | --jsonrpcserverprefixes=["http://127.0.0.1:37128/", "http://localhost:37128/"] | WASABI_JSONRPCSERVERPREFIXES=["http://127.0.0.1:37128/", "http://localhost:37128/"] |
| "DustThreshold": "0.00005" | --dustthreshold=0.00005 | WASABI_DUSTTHRESHOLD=0.00005 |
| "EnableGpu": true | --enablegpu=true | WASABI_ENABLEGPU=true |
| "CoordinatorIdentifier": "CoinJoinCoordinatorIdentifier" | --coordinatoridentifier="coinjoincoordinatoridentifier" | WASABI_COORDINATORIDENTIFIER="coinjoincoordinatoridentifier" |
| "ExchangeRateProvider": "MempoolSpace" | --exchangerateprovider=MempoolSpace | WASABI_EXCHANGERATEPROVIDER=MempoolSpace |
| "FeeRateEstimationProvider": "MempoolSpace" | --feerateestimationprovider=MempoolSpace | WASABI_FEERATEESTIMATIONPROVIDER=MempoolSpace |
| "ExternalTransactionBroadcaster": "MempoolSpace" | --externaltransactionbroadcaster=MempoolSpace | WASABI_EXTERNALTRANSACTIONBROADCASTER=MempoolSpace |
| "MaxCoinJoinMiningFeeRate": 150.0 | --maxcoinjoinminingfeerate=150.0 | WASABI_MAXCOINJOINMININGFEERATE=150.0 |
| "AbsoluteMinInputCount": 21 | --absolutemininputcount=21 | WASABI_ABSOLUTEMININPUTCOUNT=21 |
| "MaxDaysInMempool": 30 | --dropunconfirmedtransactionsafterdays=30 | WASABI_DROPUNCONFIRMEDTRANSACTIONSAFTERDAYS=30 |

_MaxDaysInMempool will only be listed in the config file after being changed from the default (30)._

### Non-Config file configurations

There are a few special switches that are not present in the `Config.json` file and are only available using the command line:

| Switch | Command Line | Environment variable |
|-------|-------------|---------------------|
| Ignore P2P transactions | --blockonly=true | WASABI_BLOCKONLY=true |
| The level of detail used during logging | --loglevel=trace | WASABI_LOGLEVEL=trace |
| Specify to log only to specific target* | --logmodes=console | WASABI_LOGMODES=console |
| The path to the directory used during runtime | --datadir="$HOME/temp/wasabi-1" | WASABI_DATADIR="$HOME/temp/wasabi-1" |
| Open wallet "WalletName" | --wallet=WalletName | WASABI_-WALLET=WalletName |
| Expose the RPC as onion service | --rpconionenabled=true | WASABI_RPCONIONENABLED=true |
| Tor will listen to this SOCKS5 port | --torsocksport=35000 | WASABI_TORSOCKSPORT=35000 |
| Tor will listen to this control port | --torcontrolport=35001 | WASABI_TORCONTROLPORT=35001 |
| Folder to use where Tor binary is located | --torfolder="$HOME/tor-browser_en-US/Browser/TorBrowser/Tor" | WASABI_TORFOLDER="$HOME/tor-browser_en-US/Browser/TorBrowser/Tor" |

*_Available options are `""` (don't log at all), `"file"` (log only to file), `"console"` (log only to console) and `"file,console"` (log to file and console)._
