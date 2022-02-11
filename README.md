# anti-keylogger
 this is basic key logger detector that run on Windows OS 
 how script work:

  1.import the list of tasks(processes) that work in the background using the the command "tasklist" that run on command by using 
  check_output() function (See Line 34) 
  for loop to interate over the task list and create from each task and object type process that will include name of the task and process id 
  then inserting them to process_list
 
2. the main read JSON File named (example_1.json) that include blacklist name of keyloggers 
 
3. flag var is flag if there is keylogger or not , recored to count task and get the process id 
 
4.run for loop over the process_cmd list that 
  4.1 if the process name include any blacklist name 
  
  4.1.1 if the user want kill the process that suspected to be keylogger 
    
  4.1.2 run function kill_logger() that get proess id 
    
  4.1.3 that fucntion run os.system to run the command "taskkill /f /im" with process id and kill it 
    
  4.2 if flag is equal to 1 then No Keylogger Detected
to add your own keylogger , you can add it to JSON file ("example_1.json") with this template 
{
    "name": "keylogger"
}


## KeyLogger
a keylogger included in the project named keylogger.exe 
disable it by kill the process in task manger 


LINK FOR KEYLOGGER 
https://mega.nz/file/ljZXDSRK#negu_weda_dcARNp6-tXCa5WtnmAXWhAVX4BFRc2GGc


 
## GITHUB 
##### https://github.com/amarhbaneen/anti-keylogger
