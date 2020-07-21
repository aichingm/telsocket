# Telsocket
Telnet-like for WebSockets

http://telsocket.org

## Installation
[Download Latest Binary](https://github.com/lafikl/telsocket/releases/latest)

Alternatively you can install using go:

```bash
go get github.com/lafikl/telsocket
```

There is also an [homebrew tap](https://pascaliske.github.io/homebrew-telsocket/) from [@pascaliske](https://github.com/pascaliske/) for installing telsocket on Mac OS X:

```bash
brew tap pascaliske/telsocket
brew install telsocket
```

## Usage

```bash
telsocket -url <url to ws server>
```
Send custom headers

```bash
telsocket -url <url to ws server> -headers name1=value1,name2=value2
```

Enable `ping` and/or `close` messages

```bash
telsocket -url <url to ws server> -ping
```
```bash
telsocket -url <url to ws server> -close
```

```bash
telsocket -url <url to ws server> -close -ping
```

After the connection is established write _ping_ or _close_ and hit enter.

Set the maximal payload size per frame (usefull to debug multi-frame messages). Replace _XXX_ with the new maximal payload size.
```bash
telsocket -url <url to ws server> -maxframesize=XXX
```

![](http://telsocket.org/images/sample.png)
