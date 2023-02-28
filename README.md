# LiTFSI_G3

## Training DPs
```
module add deepmd/2.0
dp train train.json
dp freeze -o graph.pb
dp compress -i graph.pb -o graph-compress.pb
```

## Using our models
```
module add deepmd/2.0
dp compress -i pbed3.pb -o pbed3-compress.pb
dp compress -i blypd3.pb -o blypd3-compress.pb
```

## Testing models

```
module add deepmd/2.0
dp test -m graph-compress.pb -s systems-000 -d sys_000 -n 1000
```
