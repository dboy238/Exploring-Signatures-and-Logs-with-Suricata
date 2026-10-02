# Exploring-Signatures-and-Logs-with-Suricata
In this lab, I am examining a rule in Suricata, triggering a rule, and review the alert logs, and then examining the eve.json output

<img width="320" height="113" alt="image" src="https://github.com/user-attachments/assets/4bd14aa2-7313-4d57-8fbd-412c312278b8" />

I verified the Suricata rule defined in the /home/analyst directory.

<img width="395" height="266" alt="image" src="https://github.com/user-attachments/assets/fda4d567-50e3-418e-9fd6-ea1e86e70688" />

To trigger a custom rule in Suricata, I first listed the files in the /var/log/suricata directory. Once I verified there were no files in the directory, I then ran Suricata using the custom.rules file and sample.pcap files.  

<img width="389" height="286" alt="image" src="https://github.com/user-attachments/assets/9063609b-30cb-4013-8353-3b69d058edfe" />

I then list the files in the /var/log/suricata folder and display the fast.log files to analyze the details.

<img width="392" height="505" alt="image" src="https://github.com/user-attachments/assets/830a5616-eef4-4aa6-86ff-b0ef72a38c06" />

After looking at the fast.log file, I opened the eve.json file to take a deeper look into the logs.

<img width="383" height="570" alt="image" src="https://github.com/user-attachments/assets/58d17a29-5792-49e2-baff-316251a0c8b5" />
<img width="390" height="572" alt="image" src="https://github.com/user-attachments/assets/f1c66000-aaef-418b-a3c3-fd0777e30b09" />
<img width="390" height="575" alt="image" src="https://github.com/user-attachments/assets/ebe99170-151e-49cd-a103-452e63fb9314" />

After returning the output as raw content, I used the jq command to display the entry in a simpler, easier-to-read format. For my lab, I was required to search for the severity level, which was 3, and the last event's destination IP, which was 142.250.1.102.

<img width="394" height="65" alt="image" src="https://github.com/user-attachments/assets/45f15b44-abe2-4d1a-a745-b893c6ed59ac" />

I then used the jq command to extract specific event data from the eve.json file.

After completing this lab, I have learned how to create custom rules and run them through Suricata, monitor traffic captured in a packet capture file, and examine the fast.log and eve.json output.









