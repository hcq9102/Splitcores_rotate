# Splitcores_rotate
outline:

//a. files : modified rotate algorithm rotate.hpp and benchmark hpx_rotate.cpp

//b. steps for doing the test

//c. FOLDER of local test : Local Test_splitcores

-------------------------------------
a. Source files:

1.algorithm file:    
rotate.hpp: the modified part, please see https://github.com/hcq9102/Splitcores_rotate/blob/main/rotate.hpp#L217-L275 

2.benchmark file

hpx_rotate.cpp

------------------------------------------------------------------------------------------------------------------------
b. HOW I did on rostam

1. build and install hpx on rostam:

git clone the hpx folder from Ste||ar group
modified the rotate.hpp file as shows https://github.com/hcq9102/Splitcores_rotate/blob/main/rotate.hpp#L217-L275 .
then 
$cmake flags~~~
$make
$make install

2. do benchmark test:

mkdir for benchmark : 
                      benchmark file = hpx_rotate.cpp
                      cmakelist.txt
                      
$cmake flags(find the installed HPX)    
$make

--- executable file : hpx_rotate
--- comamnd line: ./hpx_rotate --hpx:threads= x

                  get two XX.CSV files for each thread.
                  
---  if I want to try another threads y: change the name of CSV files in hpx_rotate.cpp first; 
      :wq                
      $make
      
      get new executable file hpx_rotate
      
      $./hpx_rotate --hpx:threads= y

.....
.....
-------------------------------------------------------------------------------------------

c. FOLDER of local test : Local Test_splitcores
see it(Local Test_splitcores) in this repository.
put all results together in rotate_midcores.xlsx.


