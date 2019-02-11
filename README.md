Remi Andruccioli  
February 2019  

This is a thought on the interview question dealt by Vorbrodt in this blog post:
http://blog.vorbrodt.me/?p=584

I like the implementation offered in this blog post.  
Therefore I decided to post an implementation with 2 processes instead of 2
threads.  
The difference is that 2 processes have distinct memory areas by default.  
So as one of the many possible implementations, I use Unix pipes as a way of
signaling events.  
In each loop the PID of the process is printed followed by the letter A or B.  

To compile:  
gcc -Wall -Wextra -Werror -pedantic -std=c89 cyclic_sync_processes.c

This source code is under public domain.
