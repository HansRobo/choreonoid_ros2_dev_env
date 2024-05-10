# choreonoid_ros2_dev_env

## Clone

This repository uses submodules. To clone it, use the following command:
```bash
git clone git@github.com:HansRobo/choreonoid_ros2_dev_env.git --recursive
```

## Install docker compose (v2)

```bash
sudo mkdir -p /usr/local/libexec/docker/cli-plugins
cd /usr/local/libexec/docker/cli-plugins
sudo curl -L https://github.com/docker/compose/releases/download/v2.27.0/docker-compose-linux-x86_64 -o docker-compose
sudo chmod +x docker-compose
```
## Build Container

```bash
docker compose build
```

## Start Container

```bash
docker compose up -d
```

## Development

### Enter Container

```bash
xhost localhost
docker exec -it choreonoid_workspace bash
```

### Build

```bash
colcon build --symlink-install --cmake-args -DCMAKE_BUILD_TYPE=Release
```

### Run

```bash
source install/setup.bash
ros2 launch choreonoid_ros choreonoid.launch.xml
```
