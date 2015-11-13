
best and simplest way to integrate MySQL database with c++ in code::block IDE.


Hi guys this repository is to help those guys who are facing difficulty in integrating mysql database with c++, here are some link kindly download the files from following links:



1-> Codeblock IDE/compilier:  http://cbsecsnip.in/software/swdownload.php?filename=codeblocks-10.05mingw-setup.exe
2-> mysql server: http://cbsecsnip.in/software/swdownload.php?filename=mysql-5.5.27-win32.msi


3-> sqlapi: http://cbsecsnip.in/software/swdownload.php?filename=sqlapi_trial.exe


after downloading these files collect them at one place just for ease, proceed to further step which are:
1. install all these and open mysql server and create database and table(see procedure of creation of db and table from net)

2. open code::block application then goto (File->new->Project->console application)

3. extract sqlapi to C:/ (it will create an folder named as SQLAPI) 

4. after completing step 2 escalate yourself to the step shown(select project->build option->debug option->search directories(in search option there will be an white space below that there is add button for complier head option)->add button->traverse yourself thru the C:/SQLAPI/include and add it.



5. after these : click on linker setting then under link libraries add:


C:\SQLAPI\MinGW-4.4\lib\libsqlapiddll.a


C:\Program Files(x86)\CodeBlocks\MinGW\lib\libuser32.a


C:\Program Files(x86)\CodeBlocks\MinGW\lib\libversion.a


C:\Program Files(x86)\CodeBlocks\MinGW\lib\liboleaut32.a


C:\Program Files(x86)\CodeBlocks\MinGW\lib\libole32.a


*******during performing step (11,13,14,15,16,17) of these file there will be pop-up for making them relative path(so select NO for that option).***********



Now go to Compiler and debugger option from Setting Menu in main menu and select "toolchain executables" under that change C 
complier to "gcc.exe".


CLICK OK( your work for library and include is done)



Now here we proceed for debuging part


goto your project(project name->source->main.cpp) located at left pane after this press debug option and see the path of your debug (normally it debug folder appears where u save ur project so have a look at that folder) open that and paste files from path:


C:\SQLAPI\MinGW-4.4\bin\libsqlapid.dll;

C:\Program Files\MySQL\MySQL Server 5.5\liblibmysql.dll;

clicl OK ur done setting up environment:
