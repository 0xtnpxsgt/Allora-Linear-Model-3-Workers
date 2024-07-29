# Allora With 3 Workers(Linear Model)


- You must need to buy a VPS for running Allora Worker
- You can buy from : Contabo
- You should buy VPS which is fulfilling all these requirements :

TOPIC USED - ETH
- Topic 2
- Topic 2
- Topic 3

```bash
Operating System : Ubuntu 22.04
CPU: Minimum of 1/2 core.
Memory: 2 to 4 GB.
Storage: SSD or NVMe with at least 5GB of space.
```
### Deployment - Read Carefully! 


## Step 1: Remove old project directories:
```bash
## ONE CLICK GUIDE  - RUN THIS
cd $HOME
rm -rf allora-chain
rm -rf basic-coin-prediction-node
```
## Step 2: Download & Run the setup script:
```bash
wget https://raw.githubusercontent.com/0xtnpxsgt/Allora-Linear-Model-3-Workers/main/alloraworker3.sh
chmod +x alloraworker3.sh
./alloraworker3.sh
```
Re-run the setup script after logging back in:  (if you have recently updated Docker permissions).
```bash
./allora-3W.sh
```

## Step 3: Check Node Status
After running the setup script, you can monitor the status of your workers with the following commands:
```bash
cd $HOME && cd basic-coin-prediction-node
```

- Check logs for worker-1:
```bash
docker compose logs -f worker-1
```
- Check logs for worker-2:
```bash
docker compose logs -f worker-2
```
- Check logs for worker-3:
```bash
docker compose logs -f worker-3
```


## Step 4: Check your worker logs and test the inferences using curl

```bash
# Download Checker
wget -O checkyourworker.sh https://raw.githubusercontent.com/casual1st/alloraworkersetup/main/checkyourworker.sh && chmod +x checkyourworker.sh && ./checkyourworker.sh
```

#### Run Checker
```bash
./checkyourworker.sh
```

## IMPORTANT: If you encounter any issues about inference or container, you can restart your Docker containers with the following commands:
```bash
cd $HOME && cd basic-coin-prediction-node
docker compose restar
```


