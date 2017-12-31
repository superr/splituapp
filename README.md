**splituapp** is similar to splitupdate.pl and split_updata.pl for unpacking/splitting/extracting img files from an UPDATE.APP file. The main difference being this one is written in Python2/3 instead of Perl. Additionally, **splituapp** allows you to extract specified img files where the others will only extract all img files at once. This saves a lot of time if you know which img files you want.  

Assuming **splituapp** and UPDATE.APP are in the same directory and you have a command prompt open in that directory, here are some examples.  

To extract all img files:  
```
splituapp -f UPDATE.APP
``` 
To extract only system.img and boot.img:  
```
splituapp -f UPDATE.APP -l system boot
```

You can run `./splituapp -h` (Linux) or `python splituapp -h` (Windows) to get usage instructions for the OS you are running on.  
Like splitupdate.pl and split_updata.pl, **splituapp** will do crc checksum verification on the img files after extraction if the crc binary is in the same directory the script is run from. Unfortunately I do not have the source for the binary so it is only available for Linux at this time. As a result, the crc verification will be disabled in Windows for now.

**splituapp** does not extract the images it splits from UPDATE.APP. Once the img files are split from UPDATE.APP the job is complete. If you are looking for a tool to handle system.img extraction, you can check out [SuperR's Kitchen](https://forum.xda-developers.com/apps/superr-kitchen).