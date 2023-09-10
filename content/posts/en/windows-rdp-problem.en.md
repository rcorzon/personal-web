---
title: "How to fix not being able to connect to RDP (Remote Desktop) using a Microsoft Account."
date: 2023-09-10T17:40:48+02:00
draft: false
tags:
    - Microsoft
    - Windows
    - Login
    - RDP
---

![alt text](/images/posts/en/windows-rdp-problem.en/login-error.jpg)

This is a pretty unnerving issue, not because of the failure itself, but for the lack of documentation, details and official support by Microsoft. After spending hours trying different solutions online, this is what I found that it worked for me.

There can be multiple causes of this issue, but usually this happens because **you don't have your Microsoft account password cached into your remote computer**. RDP has its credentials checked by the remote machine locally, that is, stored somewhere into the actual remote computer, and not on the cloud or an external service, even if you are using a Microsoft Account.

In order to solve this, **you will need to be able to access your remote computer**.

On your remote machine, go to the lock screen, and **choose to log in using the Microsoft password instead of the PIN or Microsoft Hello**. You only need to log in once to fix this issue.

![alt text](/images/posts/en/windows-rdp-problem.en/locking-screen.jpg)

Once you do this, everything should be ready. **Your password has been stored into your remote machine**. Open the Windows RDP app and try to log in.

![alt text](/images/posts/en/windows-rdp-problem.en/write-credentials.jpg)

You should be able to get to here now.

![alt text](/images/posts/en/windows-rdp-problem.en/cert-warning.jpg)
