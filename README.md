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
# process string java pattern.  
# change visibility in github
# how to find size of github
