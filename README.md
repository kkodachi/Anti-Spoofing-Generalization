# Anti-Spoofing Generalization

In this project we will investigate how different models work against unseen spoofing attacks.

## Setup

In carc run these commands:

```bash
pip install huggingface_hub

hf download jungjee/asvspoof5 --repo-type dataset --dry-run

hf download jungjee/asvspoof5 --repo-type dataset --local-dir /scratch1/kodachi/asvspoof5

cd scratch1/kodachi/asvspoof5

tar -xvf ASVspoof5protocols.tar
```

Run one of these:
```bash
ls flac.tar | xargs -n 1 -P 8 tar -xfs
```

Slower version if above doesn't work:
```bash
for f in flac.tar; do
    tar -xvf "$f"
done
```
