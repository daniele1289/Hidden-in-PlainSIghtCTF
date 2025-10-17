#  Writeup Hidden-in-PlainSight PicoCTF 2025

Task: You are given a seemingly ordinary JPG Image. Something is tucked away out of sight inside the file. Your task is to disvoer the hidden paload and extract the flag.
Download the jpg image provided.
Hint: Download the jpg image and read its metadata

## Steps
 Step 1) Considering this was my first CTF, at first I was unsure of what direction I shoudl take. I first downloaded the image and moved it to my current directory. The directory is the workspace in kali linux where all your programming is going towards. To check your current working directory, you can use the "pwd" command. However, once I moved the img.jpg into my current directory, I had to ensure it was actually in there. So, I utilized the command "ls", which lists all the current files in the working directory.

  <img width="898" height="103" alt="image" src="https://github.com/user-attachments/assets/e3cbe9dc-44d2-4043-88ba-a7b935a9eedd" />

  Step 2) Once I was 100% certain I had the file in my directory, it was time to start coding. I started to try and find the properties of the image to see if I could get any clues that could lead me in the right direction. First, I examined the content of the file utilizing the "exiftool" command, which reads metadata from a file. As seen below, I noticed a base 64 code was  given to me in the comments which could provide a crucial clue.

  <img width="824" height="614" alt="image" src="https://github.com/user-attachments/assets/8c64ca28-06b5-41bf-a8e9-310fc9968414" />

Step 3) At this current point, I was unsure how to decode the base-64 code given to me, so I found help from other sources. Using my knwoeldge of the "echo" command, which prints texts or variables to a terminal, I was able to deocde the base-64 message. Since I got another base-64 from my decoding, I just did a double decode.

   <img width="720" height="152" alt="image" src="https://github.com/user-attachments/assets/2285d59e-35ce-44a6-9d5d-8d9fb47a7d6e" />

   Step 4) From the previous step, the steghide essentially hides bits of data. So, I had to extract the data that was hidden in the steghide, utilizing the "extract -sf" command. Knowing that the data I now need is in flag.txt, I had to get the data out from that file. To display content in files like .txt, you cna use the "cat" command tool. As a result, I got the flag I needed to complete the CTF!
   
 <img width="395" height="279" alt="image" src="https://github.com/user-attachments/assets/1213407b-d905-4a04-8a9f-d8c51bb1e776" />


 





