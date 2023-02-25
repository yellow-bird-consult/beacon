# beacon
open repo to download scripts in CI pipelines

## Private assets
You can download private assets from releases on private repos. First you download the script with the following
command:

```bash
wget https://raw.githubusercontent.com/yellow-bird-consult/beacon/main/installs/private_asset.sh
```
This gives us the private asset script, we can then download the private asset with the following command:

```bash
sh private_asset.sh v0.0.6 wedp-aarch64-apple-darwin.tar.gz <GITHUB_TOKEN> yellow-bird-consult/wedding_planner
```

The above action will download the wedding planner docker orchestration tool for testing and development. Once you
have this you can extract the static binary with the following:

```bash
tar xzf wedp-aarch64-apple-darwin.tar.gz -O > wedp
```
We now have a static binary but we are not out of the woods yet, we need to change the permissions so we can execute the
static binary with the following command:

```bash
chmod +x ./wedp
```

We can then use the static binary tool as we need
