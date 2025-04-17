# droidkit

Containerized tools for Android development — because I don't want to install it on my machine.

## Tools

1. [`apksigtool`](https://github.com/obfusk/apksigtool)
1. [`fdroid`](https://gitlab.com/fdroid/fdroidserver)

## Example

```bash
# build the tool container
docker compose build apksigtool

# copy data you need to use
cp ./path/to/app-release.apk ./data/app.apk

# run the tool
docker compose run --rm apksigtool \
    parse --json ./data/app-release.apk \
    | jq -r ".pairs[].value._type"
```
