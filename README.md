# SmartStitchLite
Fork of original SmartStitch by MechTechnologies focusing on keeping low memory usage to safely run on virtual and/or low-end devices.

# NOTICE
**The script is still under development.**
Core components are all working but logging is not yet added. The output printed on screen while using the script is confusing and maybe useless for you.

## How to run the Console Version (For Windows, Mac, Linux Users)
1. Download the source code zip file of the latest release (Found in the releases section in this github)
2. Unzip the file to a suitable place on your device.
3. Install python edition suitable for your machine. (Python 3.7 is recommended)
4. Open a terminal and send the following command: pip install numpy pillow natsort
5. From the terminal, navigate to the directory where the source code was unzipped and run the command as per the usage details below

### Console Version Usage
```
python main.py [-h] -i INPUT_FOLDER
                    [-H SPLIT_HEIGHT]
                    [-t OUTPUT_FILES_TYPE]
                    [-b]
                    [-w {0,1,2}]
                    [-cw CUSTOM_WIDTH]
                    [-s [0-100]]
                    [-ip IGNORABLE_PIXELS]
                    [-sl [1-20]]
					[-l]
					[-ul UNIT_IMAGES]
required arguments:
    --input_folder INPUT_FOLDER, -i INPUT_FOLDER               Sets the path of Input Folder
optional arguments:
  -h, --help                                                   Shows the help message and Exits
  --split_height SPLIT_HEIGHT, -H SPLIT_HEIGHT                 Sets the value of the Rough Panel Height
  --output_files_type OUTPUT_FILES_TYPE, -t OUTPUT_FILES_TYPE  Sets the type/format of the Output Image Files
  --batch_mode, -b                                             Enables Batch Mode
  --width_enforce_type {0,1,2}, -w {0,1,2}                     Selects the Ouput Image Width Enforcement Mode
  --custom_width CUSTOM_WIDTH, -cw CUSTOM_WIDTH                Selects the Custom Image Width For Width Enforcement Mode 2
  --senstivity [0-100], -s [0-100]                             Sets the Object Detection Senstivity Percentage
  --ignorable_pixels IGNORABLE_PIXELS, -ip IGNORABLE_PIXELS    Sets the value of Ignorable Border Pixels
  --scan_line_step [1-20], -sl [1-20]                          Scan Line Step
  --low_ram, -l												   Run script in RAM efficient way (without decreasing performance*)
  --unit_images, -ul										   Maximum number of images to be loaded into RAM at any given time (only valid in LOW RAM mode)
```

### Console Version Command Example
```
python main.py -i "Review me" -H 7500 -t ".png" -l
# This will Run the application on for input_folder of "./Review me" with split_height of 7500 and output_tyoe of ".png" and batch_mode enabled
```
