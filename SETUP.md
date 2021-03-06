#Setup Steps for the Raspberry Pi

In order to run the code for this project, please follow the steps below to install the necessary dependencies. Please note that this setup in particular was completed after a fresh OS install on the pi.

<b>Step 1:</b> Update the System
Execute the following commands to ensure you are wokring with up to date libraries for your device.

    sudo apt update
    sudo apt install
    sudo apt install all
    sudo apt upgrade

<b>Step 2:</b> Install and Setup Git
Execute the following commands to install and setup Git, as well as clone the repo.

    sudo apt install git
    git config --global user.name "Your Name"
    git config --global user.email "your email address"
    git clone <url>

<b>Step 3:</b> Install OpenCV
In this step we will be installting OpenCV with the additional contributed modules. If you run into any issues during this step, it may help to refer to the linux install tutorial found on the OpenCV website.

    <b>3.1</b> Required Packages
    The following packages are required to build the OpenCV library. Execute the following commands:

        sudo apt-get install build-essential
		sudo apt-get install cmake libgtk2.0-dev pkg-config libavcodec-dev libavformat-dev libswscale-dev
		sudo apt-get install python-dev python-numpy libtbb2 libtbb-dev libjpeg-dev libpng-dev libtiff-dev libjasper-dev libdc1394-22-dev

    <b>3.2</b> Get the OpenCV Source Code
	The following commands will download the OpenCV source code from their git repository. We will also be moving to a directory to use for the download and installation process.

		cd /opt/
		git clone https://github.com/opencv/opencv.git
		git clone https://github.com/opencv/opencv_contrib.git

	<b>3.3</b> Building OpenCV using CMake
	The next portion of this setup can be strenuous on a pi and in some cases take many hours to install. To help speed up this process we will be increasing the swap space for the system.

		sudo emacs /etc/dphys-swapfile

	Now change the CONF_SWAPSIZE value from 100 to 1024. Save the file and run the following command to make the changes:

		sudo /etc/init.d/dphys-swapfile restart

	We are now ready to build OpenCV. We will start be creating a directory to work in.

		cd opencv
		mkdir build
		cd build

	Configure by executing the following:

		cmake -DCMAKE_BUILT_TYPE=Release -DOPENCV_EXTRA_MODULES_PATH=<the dir path to the contrib modules> -DCMAKE_INSTALL_PREFIX=/usr/local/ ..

	The next thing to do is build. This is the portion that will take the longest. You may have to play around with how many jobs to run in parallel. The device may freeze a few times, so if that is the case you may need to run less jobs.

		sudo make -j5 #alter the integer next to j to change the number of jobs run in parallel

    <b>3.4</b> Install Libraries
	Install the libraries by executing the following:

		sudo make install
    
    <b>3.5</b>Verify
    Verify OpenCV was installed by running the following command:

        opencv_version