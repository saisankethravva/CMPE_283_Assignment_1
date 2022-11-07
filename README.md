# CMPE_283_Assignment_1
## Team Member: Sai Sanketh Ravva (Only 1 Team Member)
## Instructor: Professor Mike Larkin  
### Questions:  
1. Describe in detail the steps you used to complete the assignment. Consider your reader to be someone 
skilled in software development but otherwise unfamiliar with the assignment. Good answers to this 
question will be recipes that someone can follow to reproduce your development steps.  
### Answer:
  step 1: Configuare a Google Cloud Platform VM that has the VMX enable.  
  
 &nbsp;&nbsp;&nbsp;&nbsp;  ![gcp](https://user-images.githubusercontent.com/38378122/200276603-e9aa5859-67fd-4a3b-9ce5-2fc333655fcd.PNG)

  step 2: Download the "cmpe283.c" source file source and "MakeFile" files from canvas provided by professor.  
  step 3: To install make tool move to root user using "sudo bash" and after instaling exit from root user then install linux headers on your VM run the below command in terminal in sudo mode.
      &nbsp;&nbsp;&nbsp;&nbsp;sudo bash 
       &nbsp;&nbsp;&nbsp;&nbsp; sudo apt install gcc make 
        &nbsp;&nbsp;&nbsp;&nbsp; exit
       &nbsp;&nbsp;&nbsp;&nbsp; sudo apt install linux-headers-$(uname-r)
      &nbsp;&nbsp;&nbsp;&nbsp;  ![img0](https://user-images.githubusercontent.com/38378122/200276808-67cc8562-9c82-423d-bceb-6e2587d106ee.PNG)


  step 4: There are 6 features that we are trying to detect base on our GCP VM.  
      &nbsp;&nbsp;&nbsp;&nbsp;a)Pinbased  
      &nbsp;&nbsp;&nbsp;&nbsp;b)probased  
      &nbsp;&nbsp;&nbsp;&nbsp;c)probased02  
      &nbsp;&nbsp;&nbsp;&nbsp;d)probased03  
      &nbsp;&nbsp;&nbsp;&nbsp;e)entry  
      &nbsp;&nbsp;&nbsp;&nbsp;f)exit (written my own strcuts for these six base on MSR index, and info on SDM, Volume 3 ch.24)  
  step 5: Create a "cpmehw3.c" file with command below      
       &nbsp;&nbsp;&nbsp;&nbsp;vi cmpehw3.c  
       &nbsp;&nbsp;&nbsp;&nbsp;write the kernel code in the above file  
      &nbsp;&nbsp;&nbsp;&nbsp;use esc and :wq to exit the file  
  step 6: Create "Makefile" using command below  
      &nbsp;&nbsp;&nbsp;&nbsp;nano Makefile  
      &nbsp;&nbsp;&nbsp;&nbsp;use ctrl+x to exit the file 
      ![image](https://user-images.githubusercontent.com/38378122/200282073-60e89943-caa2-4168-9b0c-f6b4cad1e70e.png)

  step 7: Run under the same directory with MakeFile and cmpehw3.c file in terminal  
     &nbsp;&nbsp;&nbsp;&nbsp; make  
  step 8: Use insmod command to insert and module  
     &nbsp;&nbsp;&nbsp;&nbsp; sudo insmod cmpehw3.ko  
    &nbsp;&nbsp;&nbsp;&nbsp;  ![img01](https://user-images.githubusercontent.com/38378122/200278821-6b48210b-91e6-4deb-97f1-c1a9df2f33bb.PNG)

   step 9: Use dmesg command to print the output of 6 VMX features    
    &nbsp;&nbsp;&nbsp;&nbsp;   dmesg  
    ![img1](https://user-images.githubusercontent.com/38378122/200279114-46f36799-e1a9-467e-94fa-954c26130df5.PNG)
![img2](https://user-images.githubusercontent.com/38378122/200279130-6dbcdfb3-390c-4067-ab3a-494b2b3a0e1c.PNG)
![img4](https://user-images.githubusercontent.com/38378122/200279160-4f9ebe5b-303f-4a74-90cd-7176562599ed.PNG)

    
    
       
  
