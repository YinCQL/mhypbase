# mhypbase

- This project focuses on improving the experience of private servers, not official servers.
- This project is not a protocol emulation of the original `mhypbase.dll`, users should **NOT** use it to connect to official servers.

The latest GitHub Action build artifact: [[file]](https://nightly.link/Jx2f/mhypbase/workflows/msbuild/main/mhypbase-latest.zip)

## Features

- [x] _Disable BSoD drivers_ to prevent Windows from crashing.
- [x] _Disable log uploads_ to prevent crash log upload.
- [x] _Custom channel config_ to allow users to connect to a certain dispatch server, and remove watermark.
- [x] _Custom sdk base url_ to allow users to connect to a certain sdk server without proxy.
- [x] _Verify the signature of the dispatched data_ with the public key to avoid the client error 4214.
- [x] _Encrypt account password_ with the public key, which can be decrypted by the server private key.
- [x] _Filter out the RCE packets_ to prevent the client from being fully controlled by the server.
- [ ] ......

## FAQ

> You can ask for help in [GitHub Discussions](https://github.com/Jx2f/mhypbase/discussions).

**Q: When do I use this project instead of `RSAPatch` or `Akebi-GC (RSAPatch)`?**

**A**: This project is an alternative to `RSAPatch` and `Akebi-GC (RSAPatch)`. If you already using `Akebi-GC` in private servers, it's recommended to enable the `RSAPatch` feature in `Akebi-GC` instead of using this project. If you just want to replace the dispatch RSA keys and keep updating with the latest client, it's recommended to use `RSAPatch` since it's more lightweight and easier to adapt to the latest client.

**Q: Why are those offsets hardcoded?**

**A**: ~~I'm too lazy to write pattern scanning code, and~~ some offsets are not easy to find by pattern scanning.
