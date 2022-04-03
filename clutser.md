Fortran在minicluster上的编译和运行  
调用oneAPI来编译fortran程序  

   source /home/apps/oneapi/setvars.sh intel64   


串行：   
编译：ifort -o zdcao.exe 1.f90 (1.f90为文件名，下同)   
运行：srun zdcao.exe   

并行：   
编译：mpiifort -o MPIzdcao.exe 1.f90   
运行：srun --mpi=pmi2  MPIzdcao.exe   
节点和核数在slurm的提交脚本里面设置   
 
 
 C++ FFTW编译    
 g++ -I /home/zdcao/bin/fftw/include -L /home/zdcao/bin/fftw/lib test.cpp -lfftw3 -o test (test.cpp为文件名)    
