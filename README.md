# Linux-Process-API-fork-wait-exec-
Ex02-Linux Process API-fork(), wait(), exec()
# Ex02-OS-Linux-Process API - fork(), wait(), exec()
Operating systems Lab exercise


# AIM:
To write C Program that uses Linux Process API - fork(), wait(), exec()

# DESIGN STEPS:

### Step 1:

Navigate to any Linux environment installed on the system or installed inside a virtual environment like virtual box/vmware or online linux JSLinux (https://bellard.org/jslinux/vm.html?url=alpine-x86.cfg&mem=192) or docker.

### Step 2:

Write the C Program using Linux Process API - fork(), wait(), exec()

### Step 3:

Test the C Program for the desired output. 

# PROGRAM:

## C Program to print process ID and parent Process ID using Linux API system calls
```
#include <stdio.h>
#include <sys/types.h>
#include <unistd.h>
int main(void)
{	//variable to store calling function's process id
	pid_t process_id;
	//variable to store parent function's process id
	pid_t p_process_id;
	//getpid() - will return process id of calling function
	process_id = getpid();
	//getppid() - will return process id of parent function
	p_process_id = getppid();
	//printing the process ids

//printing the process ids
	printf("The process id: %d\n",process_id);
	printf("The process id of parent function: %d\n",p_process_id);
	return 0; }
```

##OUTPUT
![Screenshot 2024-09-24 094457](https://github.com/user-attachments/assets/c3d99cf3-d33d-4964-98be-50fe82358594)

## C Program to create new process using Linux API system calls fork() and exit()
```
#include <stdio.h>
#include <sys/types.h>
#include <unistd.h>
int main(void)
{       //variable to store calling function's process id
        pid_t process_id;
        //variable to store parent function's process id
        pid_t p_process_id;
        //getpid() - will return process id of calling function
        process_id = getpid();
        //getppid() - will return process id of parent function
        p_process_id = getppid();
        //printing the process ids
//printing the process ids
        printf("The process id: %d\n",process_id);
        printf("The process id of parent function: %d\n",p_process_id);
        return 0;
}
```
##OUTPUT
![Screenshot 2024-09-24 094552](https://github.com/user-attachments/assets/eacbf45f-10a6-474e-926b-1ee36aa8705c)




## C Program to execute Linux system commands using Linux API system calls exec() family
```
#include <unistd.h>
#include <stdio.h>
#include <stdlib.h>
int main()
{
        printf("Running ps with execlp\n");
        execlp("ps", "ps", "ax", NULL);
        printf("Done.\n");
        exit(0);
}
```

##OUTPUT
![Screenshot 2024-09-24 094602](https://github.com/user-attachments/assets/c7b14f0f-82cd-408d-978d-b754e47e14fb)

# RESULT:
The programs are executed successfully.
