Consider an experimental setup consisting of a tube filled with air and closed at  one end. A vibrating source, such as a tuning fork, is placed near the open end  of the tube, generating sound waves. When the frequency of the sound matches  the natural frequency of the tube, standing waves are formed inside the tube. 
Your task is to write a Fortran program to simulate the formation of standing waves in the tube and determine the speed of sound in air, having 5 different frequencies of 5,10,20,30 and 45 Hertz.
The program should prompt the user to input the length of the tube (L) in meters. Your program should calculate and output the speed of sound (v) in air and its corresponding frequency, such that there is a spacing of 4 between them.The speed of sound can be calculated using the formula: v=2Lf

the program is written in fortran

    program standing_waves
    implicit none
    
      real :: L, v, f
      integer :: i 
      !defining integer as i because i is used as a loop counter in the do loop
    
      character (len = 30) :: format
    
      ! Prompt user to input length of the tube
      print *, "Enter the length of the tube (L) in meters:"
      read *, L
    
      ! To Loop through the desired frequencies, we use do loop
      do i = 5, 45, 5 
    
      !this will loop the program from 5 to 45 with an interval of 5
         f = real(i)
        
        ! Calculate and output the speed of sound
         v = 2.0 * L * f
         
         print *, "Frequency = ", f, "Hz"
         print *, "Speed of sound = ", v, "m/s"
         format = "(4x, a ,f4.2)"
         write(*, format)
         print *, " "
      end do

    end program standing_waves
