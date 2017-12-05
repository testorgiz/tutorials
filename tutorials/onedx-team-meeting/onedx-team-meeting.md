---
title: 1onedx-team-meeting
description: onedx-team-meeting
primary_tag: tutorial>hana
tags: [products:tech/73554900100700000996,products>sap-hana-cloud-platform\,-mobile-service-for-development-and-operations,products>sap-mobile-platform-sdk,products>sap-web-ide-1.0-plug-ins,products>sap-s-4hana,products>sap-cloud-platform, tutorial>title]
---
 
You can use:

***Text*** (including bold, italic, etc)

  **Example:**
It's very easy to make some words **bold** and other words *italic* and ***bold italic*** with Markdown.

***Headers***

  **Example:**
This is an h1 header
## This is an h2 header
###### This is an h6 header

***Lists***

  **Example:**

Sometimes you want numbered lists:

1. One
2. Two
3. Three

Sometimes you want bullet points:

* Start a line with a star
* Profit!

You can create nested lists:
![Image](ico-01.png)

![Image](/tutorials/jpg/schema.jpg)

* item1
    * one_one
    * two

***Blockquotes***

  **Example:**
In the words of Abraham Lincoln:
> Pardon my French

***Links***

  **Example:**
[Primer] [id]:
[id]: http://tut.by

Target: blank in markdown does not work
[Open in new window](http://developers.sap.com){:target="_blank"}

Anchor tag:
<a href="https://www.sap.com/developer" target="_blank">Anchor tag</a>

<http://tut.by>

<address@example.com>

***Images*** (all images are stored on GitHub, URLs are rewritten to absolute)

Format: `![Alt Text](url)`

  **Example:**
![Image](https://octodex.github.com/images/yaktocat.png)


***Code blocks:***

  **Example:**
```javascript
function fancyAlert(arg) {
  if(arg) {
    $.facebox({div:'#foo'})
  }
}
```
***Task Lists*** (Please note, this requires empty line before task list):

  **Example:**

- [x] @mentions, #refs, [links](), **formatting**, and <del>tags</del> supported
- [x] list syntax required (any unordered or ordered list supported)
- [x] this is a complete item
- [ ] this is an incomplete item

***Tables:***

  **Example:**

First Header | Second Header
------------ | -------------
Content from cell 1 | Content from cell 2
Content in the first column | Content in the second column


and

| Left-Aligned  | Center Aligned  | Right Aligned |
| :------------ |:---------------:| -----:|
| col 3 is      | some wordy text | $1600 |
| col 2 is      | centered        |   $12 |
| zebra stripes | are neat        |    $1 |

[ACCORDION-BEGIN [Step 4: ](Check the right ports are open)]

If you look at the message thrown by the client, you will find that although you explicitly call port 30030 in the `API_URL` parameter, the error message returns port 30032.  Not having the right ports open would mean more errors when trying to connect to other sites, as login requests will go through the UAA.

This means we need to make sure communications into those ports are free of blocks:

<ol type="a">
<li>  Make sure the instance has the proper ports enabled. In CAL, the configuration would look like this for this scenario from `Access points` section in the Virtual Machines tab:<br>

<br>
![Image](https://raw.githubusercontent.com/testorgiz/tutorials/edit/master/tutorials/onedx-team-meeting/img-09.png)
<img src="https://raw.githubusercontent.com/testorgiz/tutorials/edit/master/tutorials/onedx-team-meeting/img-09.png" alt="image 1"/>  </br> </li>

  <li> If you are running behind a local or corporate firewall, VPN and/or proxy, make sure traffic is coming in and out.

  There are some quick ways to check network traffic is flowing freely without installing complex tools. The following commands can be executed from a terminal or command prompt and can help uncover a network issue:
  <ol type="i">
    <li> - ping `hostname`, e.g: <i> ping http://vhcalhdbdb </i> </br>
      If, for example, you forgot to configure your hosts file, the host name will not get resolved and you will get a message similar to `Ping request could not find host xxxxx. Please check the name and try again`. Please remember to configure your hosts file with the reachable, external IP of the server. </li>

    <li> - telnet  `hostname  port`, e.g., <i> telnet  google.com  80 </i> </br>
      If the connection is somehow unavailable, you will get a message similar to <i> Could not open connection to the host, on port 22: Connect failed </i>. Any other message probably means that the server and port are reachable, although not all servers and ports are available for telnet. A `Connect failed` clearly indicates the connection cannot be established. </li>  </ol>

      </li>

</ol>

[ACCORDION-END]
