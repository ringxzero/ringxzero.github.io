- MYKINGS crypto malware on the move. 

the crypto malware incident...

it all started with a file uploaded to my crowie hoeypot. Cowrie is a medium to high interaction SSH and Telnet honeypot designed to log brute force attacks and the shell interaction performed by the attacker.  the attacker was able to get the file in. looking at the file we see this. https://www.virustotal.com/gui/file/6f445252494a0908ab51d526e09134cebc33a199384771acd58c4a87f1ffc063/detection
a crypto miner known as Myking, looking to the file i was not sure there was much more to the story. but after i played with splunk and imported some data into it. i saw this. 





clearly this was the attcker uploading the file, thankfully he left a lot for us to look at. IP his webserver he uses to wget his elf based crypto malware AND his crypto address for a public miner pool being used to host his hacked mining servers... 

first, The malware hosting website.





if you were to wget http://IP/systemd you would see a file start to download. that is were the crypto miner is stored to grab when they please. you can then see his attempt to add it to his miner pool. its a XRP crypto miner pool striclty i believe . (see below)








sometimes. there is a lot more that meets the eye. and that's why i love splunk....