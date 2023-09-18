# Quick CMS Stored XSS v6.7

## Author: (Sergio)

**Description:** A Cross-Site Scripting (XSS) vulnerabilitie in Quick CMS v6.7 allows a local attacker to execute arbitrary code via a crafted script to the to the Content - Name in the Pages Menu.

**Attack Vectors:** Scripting A vulnerability in the sanitization of the entry in the Nmae of Content of Pages Menu allows injecting JavaScript code that will be executed when the user accesses the web page.

---

### POC:


When logging into the panel, we will go to the "Content - Name" section off Pages. 

![XSS Payload Name](https://github.com/sromanhu/Quick-CMS-Stored-XSS---Pages-Content/assets/87250597/3896883e-56c7-418f-9687-b94afd219725)





We edit that Content Settings and see that we can inject arbitrary Javascript code in the Name field.


### XSS Payload:

```js
<svg/onload=alert(document.domain)>
```


In the following image you can see the embedded code that executes the payload in the main web.
![XSS resultado Name](https://github.com/sromanhu/Quick-CMS-Stored-XSS---Pages-Content/assets/87250597/684b6c4a-880f-4efc-a572-044daae9c7b5)





</br>

### Additional Information:
https://opensolution.org/cms-system-quick-cms.html

https://owasp.org/Top10/es/A03_2021-Injection/
