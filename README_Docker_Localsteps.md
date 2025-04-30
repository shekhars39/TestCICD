# GAGA Local instance steps

## Have AZ CLI installed local
```bash
winget install --exact --id Microsoft.AzureCLI
```
## How to build the docker image


#### Step 1: Run from repo folder
```bash
docker build -t gaga GAGA
```

#### Step 2: Run docker image locally
```bash
$ docker run --rm -d -p 4000:3838 gaga
```

#### Step 3: Push to ACR
```bash
az login
az acr login --name desrdacr
docker tag gaga desrdacr.azurecr.io/gaga
docker push desrdacr.azurecr.io/gaga
```
#### Step 4: Run Web App
```bash
#### Run the GAGA
```

