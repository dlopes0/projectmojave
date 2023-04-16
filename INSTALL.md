# Instructions
## How to Setup
### 1. Cloning the Server
#### 1.1. Install git:
**on Alpine Linux** 
```
apk add git
```
**on Debian/Ubuntu**
```
apt-get install git
```
#### 1.2. Clone
```
git clone https://github.com/dlopes0/projectmojave.git
```
#### 1.3. Change directory
```
cd projectmojave
```
### 2. Install OpenJDK 17
on Alpine Linux
```
apk add openjdk17-jre-headless
```
on Debian/Ubuntu
```
apt-get install openjdk-17-jre-headless
```
### 3. Run Minecraft Forge installer
```
java -jar forge-1.12.2-14.23.5.2859-installer.jar --installServer
```
### 4. Run minecraft_server for the first time
```
java -jar minecraft_server.1.12.2.jar
```
### 5. Accept eula.txt
Change to
```
eula=true
```
### 6. Run minecraft_server again
```
java -jar minecraft_server.1.12.2.jar
```
### 7. Stop server after it loads completely with:
```
/stop
```
### 8. Change plugins-dir variable at config/sponge/global.conf to "${CANONICAL_GAME_DIR}/plugins"
```
plugins-dir="${CANONICAL_GAME_DIR}/plugins"
```
### 9. You're all set! Run minecraft_server each time to start the server.
```
java -Xmx6G -Xms32M -XX:-UseVMInterruptibleIO -XX:+UseConcMarkSweepGC -XX:+CMSIncrementalPacing -XX:ParallelGCThreads=$CPU_COUNT -XX:+AggressiveOpts -jar minecraft_server.1.12.2.jar --nogui
```
