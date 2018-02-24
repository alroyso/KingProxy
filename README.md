# KingProxy
A proxy can forward http to socks and socks to socks base rule
## Feature
* Http(s) proxy
* Forward http to socks5 proxy
* Forward socks to another sub socks proxy
* Partial support surge rule
## Requirement
* Swift4
* Xcode9
* iOS 10.0/macOS 10.12
## Usage
```swift
ACL.shared?.load(configFile: "your config file")

// http
httpProxy = KingHttpProxy(address: "127.0.0.1", port: 8898)
httpProxy.forwardProxy = ForwardProxy(type: .socks5, host: "127.0.0.1", port: 8899)
httpProxy.start()

// socks
socksProxy = KingSocksProxy(address: "127.0.0.1", port: 8898)
socksProxy.forwardProxy = ForwardProxy(type: .socks5, host: "127.0.0.1", port: 8899)
socksProxy.start()
```
## Install
* Carthage
`github "purkylin/KingHttpProxy" "master"`
## TODO

