# Move Gensyn Nodes to New VPS

*By Ez Labs Nodes — Jul 27, 2025*

## Step 1: Make 100GB Swap

```bash
rm -rf create-swap-100.sh && wget https://raw.githubusercontent.com/ezlabsnodes/autoinstall/main/create-swap-100.sh && chmod +x create-swap-100.sh && sudo ./create-swap-100.sh
```

## Step 2: Install Dependency

```bash
rm -rf depedency-nodejs.sh && wget https://raw.githubusercontent.com/ezlabsnodes/autoinstall/main/depedency-nodejs.sh && chmod +x depedency-nodejs.sh && sudo ./depedency-nodejs.sh
```

## Step 3: Create Directory Ezlabs

```bash
mkdir ezlabs
```

Copy three files to `/root/ezlabs/`:
- `swarm.pem`
- `userApiKey.json` 
- `userData.json`

## Step 4: Running Gensyn Node Use Systemd

```bash
cd && rm -rf officialauto.zip systemd.sh && wget -O systemd.sh https://raw.githubusercontent.com/ezlabsnodes/gensyn/main/systemd.sh && chmod +x systemd.sh && ./systemd.sh
```

✅ **ALL DONE**

## Check Logs

```bash
journalctl -u rl-swarm -f -o cat
```

## Check All Logs

```bash
cat ~/rl-swarm/logs/swarm_launcher.log
```
