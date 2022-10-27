# Project 7 - WordPress Pen Testing

Time spent: **8** hours spent in total

> Objective: Find, analyze, recreate, and document **five vulnerabilities** affecting an old version of WordPress

## Pen Testing Report

### 1. (Required) Vulnerability Name or ID: WordPress 4.1-4.2.1 - Unauthenticated Genericons Cross-Site Scripting (XSS)

- [ ] Summary: Using the default settings, a logged-in administrator can trigger a series of actions that would allow the hacker to run arbitrary code on the server through theme and plugin editors. The hacker could even alter the administrator password, set up new administrator accounts, or perform any action that is performable by a logged in administrator on the target system.
  - Vulnerability types: WordPress Unauthenticated Stored Cross-Site Scripting (XSS)
  - Tested in version: 4.2
  - Fixed in version: 4.2.1
- [ ] GIF Walkthrough: Uploaded
- [ ] Steps to recreate: Run wpscan --url http://wpdistillery.vm --random-user-agent in Kali VM. inject JavaScript in 
WordPress comments. The script is triggered when the comment is viewed.

- [ ] Affected source code:
  - [Link 1](https://core.trac.wordpress.org/browser/tags/version/src/source_file.php)
  
### 2. (Required) Vulnerability Name or ID: WordPress 4.1-4.2.1 - Unauthenticated Genericons Cross-Site Scripting (XSS)

- [ ] Summary: cross-site scripting vulnerability existed in an HTML file shipped with  Genericons packages included in the Twenty Fifteen theme as well as a number of popular plugins
  - Vulnerability types: Unauthenticated Genericons Cross-Site Scripting (XSS)
  - Tested in version: 4.2
  - Fixed in version: 4.2.2
- [ ] GIF Walkthrough: Uploaded
- [ ] Steps to recreate: Exploit the vulenrability within the HTML file. Use cross-site scripting in the genericons packages that are a part of the theme and plugins.
- [ ] Affected source code:
  - [Link 1](https://core.trac.wordpress.org/browser/tags/version/src/source_file.php)

### 3. (Required) Vulnerability Name or ID: WordPress 3.7-4.4.1 - Local URIs Server Side Request Forgery (SSRF)

- [ ] Summary: The filter does not validate for 0.0.0.0:port. Wordpress installations can allow unwanted scrape/scan requests to be sent on behalf of the user caused by the attacker, incuding private connections.
  - Vulnerability types: Local URIs Server Side Request Forgery (SSRF)
  - Tested in version: 4.2
  - Fixed in version: 4.2.7
- [ ] GIF Walkthrough: Uploaded
- [ ] Steps to recreate: Attacker forces the victim to send get requests to the server. The URL fails to validate the user's intention to send a scrape request.
- [ ] Affected source code:
  - [Link 1](https://core.trac.wordpress.org/browser/tags/version/src/source_file.php)

## Assets

List any additional assets, such as scripts or files
PowerShell scripts in Course Portal

## Resources

- [WordPress Source Browser](https://core.trac.wordpress.org/browser/)
- [WordPress Developer Reference](https://developer.wordpress.org/reference/)
- [Wordpress Support](https://wordpress.org/support/wordpress-version/version-4-2-2/)
- [Hackerone Internal GET](https://hackerone.com/reports/110801)

GIFs created with  ...
[ScreenToGif](https://www.screentogif.com/) for Windows

## Notes

Describe any challenges encountered while doing the work
I was confused because the link initially did not work but then I had to change the code in the file to then allow me to go to the link instead of typing in the IP address in my browser.

## License

    Copyright [2022] [Apache]

    Licensed under the Apache License, Version 2.0 (the "License");
    you may not use this file except in compliance with the License.
    You may obtain a copy of the License at

        http://www.apache.org/licenses/LICENSE-2.0

    Unless required by applicable law or agreed to in writing, software
    distributed under the License is distributed on an "AS IS" BASIS,
    WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
    See the License for the specific language governing permissions and
    limitations under the License.
