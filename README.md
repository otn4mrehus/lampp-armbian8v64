# Lampp-Armbian8v64
## Container
```
+ Single Web [A]
    Web [A]  
    DB  [A]  --------------------->    --------------------------------
+ Multi Web [B]                        |                              |
  - Web B.1                            |                              |
    DB  B.1  --------------------->    |            1 (one)           |
  - Web B.2                            |           PHPMyAdmin         |
    DB  B.2  --------------------->    |         (ALL-Database)       |
  - Web B.3                            |    DB [B.1, B.2, B.3, B.4]   |
    DB  B.3  --------------------->    |                              |
  - Web B.4                            |                              |
    DB  B.4  --------------------->    --------------------------------
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
#### Start | Restart 
```
docker-compose -f docker-compose_MultiDB.yaml -p 'lampp' restart 
```
#### Stop 
```
docker-compose -f docker-compose_MultiDB.yaml -p 'lampp' stop
```
#### Remove 
```
docker-compose -f docker-compose_MultiDB.yaml -p 'lampp' down
```
#### Remove All
```
docker-compose -f docker-compose_MultiDB.yaml -p 'lampp' down -v --remove-orphans
```

## RUN
```
PHPMyAdmin WEB       -->  http://ip-address:1555 
WEB           [A]    -->  http://ip-address:1525 
WEB           [B.1]  -->  http://ip-address:1510
WEB           [B.2]  -->  http://ip-address:1520
WEB           [B.3]  -->  http://ip-address:1530
WEB           [B.4]  -->  http://ip-address:1540 
```

