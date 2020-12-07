!! This program demonstrates (1) how to skip the first line, and (2) how to read data organized in a matrix

program read_matrix
   implicit none
   
   !! Part 1: Define all the variables
   integer :: num = 365, i
   
   
   !! Part 2: Create array and use them to read the data from dataset and do the computation   
   integer, allocatable :: date_num(:)                     !! Read the first column, day numbers  
   real(kind=8), allocatable :: temp_min(:)                !! Read min temperature
   real(kind=8), allocatable :: temp_max(:)                !! Read max temperature
   real(kind=8), allocatable :: temp_average(:)            !! Calculate average temperature
   allocate(date_num(num), temp_min(num), temp_max(num), temp_average(num))
   
   
   !! Part 3: Specify the dataset
   open(1, file = 'calgary temperature 2019.txt')
   
   
   !! Part 4: Read minimum and maximum temperature, and calculate average temperature
   do i = 1, num
       read(1,*) date_num(i), temp_min(i), temp_max(i)     !! Read the data
       temp_average(i) = (temp_min(i) + temp_max(i))/2     !! Calculate average temperature
       print*, date_num(i), temp_average(i)                !! Print out the results   
   end do
   
   deallocate(date_num, temp_min, temp_max, temp_average)
   
end program
