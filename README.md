# Firmware - README.md

## Установка

1. Установить чистую [Ubuntu 20.04 lts](https://releases.ubuntu.com/focal/).
2. Сделать обновление ссылок и обновление пакетов ОС с помощью команд:
  ```
  sudo apt update
  sudo apt upgrade
  ```
2. Установить [Ros Noetic](http://wiki.ros.org/noetic/Installation/Ubuntu).
3. Установить пакеты catkin tools:
  ```
  sudo apt-get install python3-catkin-tools
  ```
5. Установить mavros:
  ```
  sudo apt-get install ros-noetic-mavros ros-noetic-mavros-extras
  ```
5. Установка geographiclib:
  ```
  wget https://raw.githubusercontent.com/mavlink/mavros/master/mavros/scripts/install_geographiclib_datasets.sh
  sudo chmod +x ./install_geographiclib_datasets.sh
  sudo ./install_geographiclib_datasets.sh
  ```
6. Скачиваем симулятор:
  ```
  git clone https://github.com/LeekaiDel/Firmware.git
  sudo bash ~/Firmware/Tools/setup/ubuntu.sh
  sudo apt install python3-packaging
  sudo apt install python3-jinja2
  sudo apt install python3-toml
  sudo apt update
  sudo apt upgrade
  ```
7. Building:
  ```
  cd Firmware
  make clean
  DONT_RUN=1 make px4_sitl_default gazebo
  ```

## Запуск

9. Затем в директории Firmware прописываем следующие команды:
  ```
  . start.sh
  ```
10. Теперь мы можем запустить симулятор командой:
  ```
  roslaunch px4 aerobot_third_test.launch
  ```
