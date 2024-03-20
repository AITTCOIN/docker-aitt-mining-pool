### How to start a docker mining pool by AITTCOIN official mining pool images in few seconds:

### Step 0: rent an vps with ubuntu/debian system

A public mining pool shouw have at least 4CPUs 8G RAM and 100GB space

install docker https://docs.docker.com/engine/install/ubuntu/

### Step 1:

    wget http://bin.aittcoin.org/aitt_mining_pool.tar

    you should check the SHA256:

    SHA256: fccc173c4ad1189127d125c511776a84a999534d6f36b9ae8d8ae8479f48086d

### Step 2:

    docker load -i aitt_mining_pool.tar

### Step 3:

    docker run -it aitt_mining_pool
    
### Step 4:

    /root/pool/start.sh

    The shell script will create a new address for your mining pool
    Waiting for aittcoind to synchronize with the mainnet then you will see this
    
  ![image](https://github.com/AITTCOIN/docker-aitt-mining-pool/assets/161400084/f423c996-6e78-42ad-a9ff-7fb2b57565e2)

    Ctrl+C 
            close pm2 log 
            
    pm2 log 
            show the mining pool log.
            
    ip a 
            check your container ip address
            
    Ctrl+P Ctrl+Q
            leave your container
            
    docker attach yourcontianer
            enter your container
    
### Step 5:

Set up your nginx 

Your mining pool banckend http port is 8080

Your mining stratum backend port is 10008, 10016, 10032

The backend ip is your container ip (eg: 172.17.0.2 )




    
