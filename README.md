# Mirror of `minio` and `mc` binaries

MinIO has a very slow CDN, so here we mirror some `.deb` files:

```
# sha256sum:
brew install coreutils

wget -c https://dl.min.io/server/minio/release/linux-amd64/archive/minio_20221117232009.0.0_amd64.deb
wget https://dl.min.io/server/minio/release/linux-amd64/archive/minio_20221117232009.0.0_amd64.deb.sha256sum

wget -c https://dl.min.io/server/minio/release/linux-arm64/archive/minio_20221117232009.0.0_arm64.deb
wget https://dl.min.io/server/minio/release/linux-arm64/archive/minio_20221117232009.0.0_arm64.deb.sha256sum

wget -c https://dl.min.io/client/mc/release/linux-amd64/archive/mcli_20221117212039.0.0_amd64.deb
wget https://dl.min.io/client/mc/release/linux-amd64/archive/mcli_20221117212039.0.0_amd64.deb.sha256sum

wget -c https://dl.min.io/client/mc/release/linux-arm64/archive/mcli_20221117212039.0.0_arm64.deb
wget https://dl.min.io/client/mc/release/linux-arm64/archive/mcli_20221117212039.0.0_arm64.deb.sha256sum

sha256sum -c "minio_20221117232009.0.0_amd64.deb.sha256sum"
sha256sum -c "minio_20221117232009.0.0_arm64.deb.sha256sum"
sha256sum -c "mcli_20221117212039.0.0_amd64.deb.sha256sum"
sha256sum -c "mcli_20221117212039.0.0_arm64.deb.sha256sum"
```
