#StegExpose

##Description

##Usage
*java -jar StegExpose.jar [directory] [speed] [threshold] [csv file]*
where
*[directory]* - direcotry containing images to be diagnosed
*[speed]* - Optional. Can be set to 'default' or 'fast' (the default value is 'default'). default mode will try and run all detectors whereas fast mode will skip the expensive detectors incase cheap detectors give a strong result.
*[threshold]* - Optional. The default value here is xxxx and determines the the level at which files considered to hide data or not. A floating point value between 0 and 1 can be used here to update the threshold. 
*[csv file]* - Optional. Name of the csv (comma seperated value) file that is to be generated. that If left blank, the program will simply output to the console. 


##Example
Basic usage of Stegexpose, providing a directory of images as the only argument

*java -jar StegExpose.jar testFolder*

Produce a steganalytic report in the form of a csv file named 'steganalysisOfTestFolder'

*java -jar StegExpose.jar testFolder default default steganalysisOfTestFolder*

Updating the threshold and running the program in fast mode to save time.

*java - jar StegExpose testFolder fast 0.3*

##Bugs
Component detecters do not all generate results for all images meaning the final steganalytic diagnosis in not always based on all four detectors.

##Sources
