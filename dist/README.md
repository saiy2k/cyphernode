# Setup multiple lightning nodes

1. Stop Cyphernode by running `./dist/stop.sh`

2. Run the following sequence of commands:
```
cd dist/cyphernode/
cp -rp lightning lightning2
cd lightning2
```
vim config #change node name
```
rm lightningd-regtest.pid
cd regtest
rm *
```

3. Edit dist/docker-compose.yaml
  1. Replicate lightning block 
  2. Rename to lightning2 
  3. Change the volume directory to lightning2
  4. Change host port to avoid conflict

4. Run `./dist/start.sh`
