---
title: "Quartz Notes"
---

For more details:
https://quartz.jzhao.xyz/tags/setup/

# 2022-04-11
Mainly updated because I wanted "last updated" to work properly (it does now!)

There is now a `make update` command, but to get there you need to update the [Makefile](https://github.com/jackyzha0/quartz/blob/hugo/Makefile) manually.

Note the update is selective, so in my case, I had to manually add:
```
# To be able to locally diagnose why gh actions failing
go install github.com/jackyzha0/hugo-obsidian@latest

# Get generation working (otherwise dies!)
git checkout -p upstream/hugo -- assets/indices

# Get styles working (note if you run this that would let you fix indices as well)
git checkout -p upstream/hugo -- assets
```