# Docker（Node.js + Angular + 日本語化等）（Mac用）

## メモ

- bashで`node:15.3.0-buster-slim`をビルドする

```bash
docker image build \
-f .devcontainer/Dockerfile \
-t test .
```

- `node:15.3.0-buster-slim`に、bashでアクセスする

```bash
docker container run \
-it \
--name test \
-h test \
node:15.3.0-buster-slim /bin/bash
```
