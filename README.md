# vesc_files_rc_car

Rep structure:

  1. .Zip  files *Vesc_install_folder.zip* contains bldc-firmware, bldc-tools, and hardware folders
  2. Configuarations for Vesc controllers being used for the project
  
Alternative way to install:
from (https://github.com/jetsonhacks/installBLDC/blob/master/installBLDC.sh)

cd $ROOT
echo "Installing BLDC Tool prerequisites"
sudo apt-get install qtcreator qt-sdk libudev-dev libqt5serialport5-dev 
echo "Fetching bldc-tool source code"
git clone https://github.com/vedderb/bldc-tool
cd bldc-tool
echo "Building bldc-tool from source"
qmake -qt=qt5
make clean && make
cd $ROOT
git clone https://github.com/mit-racecar/hardware.git
echo "You should now be able to run BLDC_Tool from the ~/bldc-tool directory"
echo "The VESC firmware is in ~/bldc-tool/firmwares"
echo "The RACECAR VESC configuration files are in ~/hardware/vesc"
