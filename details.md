### Here are the main unresolved that I encountered during the process of the assignement. 

GoPro Fusion Studio 1.3 does not allow to process a whole directory. In this last try to process a whole directory with the software alone, here is my command line :

```C:\Program Files\GoPro\Fusion Studio 1.3>FusionStudio_x64.exe --front -d C:\Users\Anais\Desktop\gopro_fusion\FRONT\DCIM\103GFRNT --firstFrame GF055000.JPG --lastFrame GF055003.JPG --back -d C:\Users\Anais\Desktop\gopro_fusion\BACK\DCIM\103GBACK --firstFrame GB055000.JPG --lastFrame GB055003.JPG -o -d C:\Users\Anais\Desktop\gopro_fusion -p 0 --pc 1```

The details of the options of this command line can be found in the user documentation. The one option that I tried to use is -d to process a whole directory.
Here is the output that I got : 

```C:\Program Files\GoPro\Fusion Studio 1.3>```
```default GST cache is set to ' "C:/Users/Anais/AppData/Local/FusionStudio_x64/cache/fusionStudioCache-1.12.4.bin" '```
```[SuperbankCommandLineParser] "GoPro Fusion Studio v1.3.0.400 (b8b265a0)"```
```[Utils] Could not parse time "GB055000.JPG"```
```[SuperbankCommandLineParser] The given firstFrame is invalid. Using default value.```
```[Utils] Could not parse time "GB055003.JPG"```
```[SuperbankCommandLineParser] The given lastFrame is invalid. Using default value.```
```[SuperbankCommandLineParser] Output directory is not writable "C:/Program Files/GoPro/Fusion Studio 1.3"```
 
**I found no debugging tool or mean to know to what extent were the frames invalid.** The ```--advancedDebug``` option does not write any images in this debug folder. The ```--logLevel 4+``` (debug level) option does not provide any info either. 
The output directory never seems to be writable, even when changing the paths/folder/creating a new one.```



When uploading the images to Mapillary, I got this error : 

```Traceback (most recent call last):```
```  File "C:\python27\Scripts\mapillary_tools", line 60, in <module>```
```    command.run(args)```
 ``` File "C:\python27\lib\site-packages\mapillary_tools\commands\process_and_upload.py", line 138, in run```
 ```   post_process(**({k: v for k, v in vars_args.iteritems()```
```NameError: global name 'post_process' is not defined```

It seems like the post_process function prevented the user_process to complete successfully. 
