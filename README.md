## twitter-to-bsky importer

Import your Twitter archive into a Bluesky account.

Usage:

```bash
# Get an archive from https://twitter.com/settings/download_your_data
# Unzip a Twitter archive so the assets/ folder is in the same directory as main.py
export BSKY_USERAME="yourname.bsky.social"
export PASSWORD="yourpassword"
pip install atprototools==0.0.6
python main.py
```

### Known problems

Bluesky's UI currently renders timestamps based on the indexedAt field (i.e., when the skoot was skooted) rather than the createdAt field (when the skoot CLAIMS it was skooted).

The code here currently tries to post skoots with the old timestamps, but the Bluesky UI will not render them so. It used to, and then Paul probably patched the bug ^^


### See also

https://github.com/ianklatzco/atprototools -- underlying library
