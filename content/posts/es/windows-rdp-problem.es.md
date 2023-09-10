---
title: "Como solucionar el error de no poder hacer login en Escritorio Remoto de Windows usando una Cuenta Microsoft"
date: 2023-09-10T17:40:48+02:00
draft: false
tags:
    - Microsoft
    - Windows
    - Login
    - RDP
---

![alt text](/images/posts/en/windows-rdp-problem.en/login-error.jpg)

Este problema es bastante molesto, no ya por ser un bug, si no también debido a la falta de documentación oficial por parte de Microsoft que explique posibles soluciones. Después de indagar en internet durante unas cuantas horas he encontrado esta solución que parece ser la correcta.


Puede haber múltiples causas de este fallo, pero normalmente ocurre porque **la contraseña de la cuenta de Microsoft no está guardada localmente en el ordenador remoto**. La aplicación de Escritorio Remoto comprueba la contraseña con un valor guardado de forma local, no accediendo a un servicio online o a Live.com.

Para solucionar este error, **necesitas acceder físicamente a tu ordenador remoto**.


En tu ordenador remoto, ve a la página de bloqueo (con Win+L, por ejemplo) y elige **hacer login usando una contraseña en vez de un PIN u otro método de Windows Hello**. Sólo necesitarás realizar este proceso una vez.

![alt text](/images/posts/en/windows-rdp-problem.en/locking-screen.jpg)

Una vez lo hagas, todo debería estar listo. **Tu contraseña ha sido guardada en el ordenador en remoto**. Accede ahora a otra máquina Windows e intenta hacer login.

![alt text](/images/posts/en/windows-rdp-problem.en/write-credentials.jpg)

Deberías ser capaz de llegar hasta este punto.

![alt text](/images/posts/en/windows-rdp-problem.en/cert-warning.jpg)

