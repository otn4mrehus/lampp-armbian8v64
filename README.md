# Lampp-Armbian8v64
## Container
```
+ Single Web [A]
    Web [A]  
    DB  [A]  --------------------->    ------------------------------
+ Multi Web [B]                        |                            |
  - Web B.1                            |                            |
    DB  B.1  --------------------->    |                            |
  - Web B.2                            |             (1)            |
    DB  B.2  --------------------->    |         PHPMyAdmin         |
  - Web B.3                            |       (ALL-Database)       |
    DB  B.3  --------------------->    |                            |
  - Web B.4                            |                            |
    DB  B.4  --------------------->    ------------------------------
```   

## Download
```
git clone https://github.com/otn4mrehus/lampp-armbian8v64.git
cd lampp-armbian8v64
```

## Build
```
docker-compose -f docker-compose_MultiDB.yaml -p 'lampp' up --build -d
```

## Manage Container
### Start | Restart 
```
docker-compose -f docker-compose_MultiDB.yaml -p 'lampp' restart 
```
### Stop 
```
docker-compose -f docker-compose_MultiDB.yaml -p 'lampp' stop
```
### Remove 
```
docker-compose -f docker-compose_MultiDB.yaml -p 'lampp' down
```
### Remove All
```
docker-compose -f docker-compose_MultiDB.yaml -p 'lampp' down -v --remove-orphans
```

## RUN
```
WEB [A]  -->  http://ip-address:2525 
WEB [B]  -->  http://ip-address:2525 
```

