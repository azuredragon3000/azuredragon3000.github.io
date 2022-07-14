# batch file basic.  

@echo on
cd /d c:\ -> go to c disk
cd ../../ -> back to previous folder

COPY C:\a.txt D:\b.txt -> copy file

setup enviroment then we can use -> ' call '

example we have a file a.exe we can call directly to run
c:\a.exe param1 param2

cd %~d0%~p0 -> go to currently path
rem abc -> comment in batch file
del log\*.* /s /q -> delete folder log
python p.py -> call python script but we have to define python tool in enviroment
md log -> create new folder log
md log\abc -> create new folder abc in log folder
if exist log rd /S /Q log -> if exit folder log delete log ? what is different with del ??
del /F /Q and rd /S /Q

sub funtion in batch


: exit_safe -> define sub function
call :exit_safe
GOTO : eof -> >???

EXIT -> exit batch file
PAUSE -> pause batch file

for loop
FOR /L %%G IN (1,1,%MARCO_ITERATION_COUNT%) DO (call :subroutine "%%G")


# gradle script basic.  

## build and sign android project with jks
    @ECHO ON
    echo build azuredragon 
    && cd C:\Users\azuredragon\AndroidStudioProjects\main_workspace\azuredragon 
    && call .\gradlew assembleDebug --> run debug
    && call .\gradlew bundleRelease --> run release
    && cd C:\Users\azuredragon\appData\Local\Android\Sdk\platform-tools --> goto platform tool
    && adb install C:\Users\azuredragon\AndroidStudioProjects\main_workspace\azuredragon\app\build\outputs\apk\debug\app-debug.apk  -> install it in simulator
    && jarsigner -keystore C:\Users\azuredragon\workspace\androidJava\resources\Pool_apk\azuredragon.jks
    C:\Users\azuredragon\AndroidStudioProjects\main_workspace\azuredragon\app\build\outputs\bundle\release\app-release.aab key0  -storepass "xxxxx" -keypass "xxxxx" 
    -> sign it with jarsigner tool
    && echo passed || echo failed --> show result failed or pass

## create jks for new module

    @ECHO ON
    set DIR=C:\Users\azuredragon\workspace\androidJava\resources\Pool_apk
    cd %DIR%
    keytool -genkey -v -keystore app201.jks -alias key0 -keyalg RSA -keysize 2048 -validity 10000 --> create jks use keytool  
## open emulator

    @echo on
    set DIR=C:\Users\azuredragon\AppData\Local\Android\Sdk\emulator
    cd %DIR%
    cmd /k emulator -avd Pixel_2_API_30

## clean data for emulator

    @echo on
    set DIR=C:\Users\azuredragon\AppData\Local\Android\Sdk\emulator
    cd %DIR%
    cmd /k emulator -avd Pixel_2_API_30 -wipe-data

# change visibility in github
go to setting project  
<img src="https://github.com/azuredragon3000/azuredragon3000.github.io/blob/main/settting project.png"  />  
scroll down to danger zone to change visibility    
<img src="https://github.com/azuredragon3000/azuredragon3000.github.io/blob/main/dangerzone.png"  />  

# generate token github  
go to setting account as below  
<img src="https://github.com/azuredragon3000/azuredragon3000.github.io/blob/main/setting.png"  />  
go to developer setting  
<img src="https://github.com/azuredragon3000/azuredragon3000.github.io/blob/main/developersetting.png"  />   
generate token  
<img src="https://github.com/azuredragon3000/azuredragon3000.github.io/blob/main/generate token github.png"  />   

# how to find size of github
to find size the respository github as below image  
<img src="https://github.com/azuredragon3000/azuredragon3000.github.io/blob/main/2022-07-14_14h58_21.png"  />  
remember for free user we only have 500 MB for stored data  
