---
title: How to use the Visual Studio Remote Debugger ?
author: 0xlay
date: 2022-08-27 10:00:00 +0300
categories: [Tutorial]
tags: [visual-studio, debug]
math: true
mermaid: true
image:
  path: /assets/posts/vs-remote-debugging/vs-preview.png
  width: 800
  height: 500
---

<div align="justify">
Hi, there. Often, we need to debug an unstable application that can destroy our system and because so we use a virtual machine. For debugging on the VM or other remote pc, Microsoft developed remote debugging tools which supporting since Visual Studio 2012 and later. 
In this article, we talk about remote debugging with the visual studio. First, we should prepare the virtual machine that we will use to test some apps. Then we are going to the <a href=" https://docs.microsoft.com/en-us/visualstudio/debugger/remote-debugging">microsoft website</a>, and download the tools for our Visual Studio.
</div>

![](/assets/posts/vs-remote-debugging/tools-table.png)

<div align="justify">
After downloading tools, transfer them to the virtual machine and install. Then we are going to configure the VS tools. First, we should compile an app that we will use for tests, and move this test app in the virtual machine. Next step we should run the tool that we have installed on the virtual machine. 
</div>

> Path to tools: ```C:\Program Files\Microsoft Visual Studio 16.0\Common7\IDE\Remote Debugger\x64\msvsmon.exe```
{: .prompt-tip }

<div align="justify">After we have got window, and we should accept configure remote debugging.
</div>

![](/assets/posts/vs-remote-debugging/remote-debugging-config.png){: width="350" height="350" }

<div align="justify">Then we should open Tools->Options (CTRL + O), and set checkboxes as shown in the screenshot.
</div>

![](/assets/posts/vs-remote-debugging/tools-options.jpg){: width="350" height="350" }

<div align="justify">
Next step we should switch to the host machine and run the visual studio as administrator. After we opening Debug->Attach to Process. In the “Connection type” field, we are setting “Remote (no authentication)”, and the “Connection target:” field, we are setting name and port, which we are looking for in the visual studio remote debug tools window on the VM. Then we should press the find button, select the PC and connect.
</div>

![](/assets/posts/vs-remote-debugging/vs-attach-to-process.png){: width="800" height="500" }

<div align="justify">
After we are going to run the test application on the virtual machine, and attach to the process from the visual studio, and begin debugging the test app.
</div>