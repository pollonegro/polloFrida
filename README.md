# polloFrida
Now.. Hacking with Frida Powers!



1. Preparación del laboratorio


- DISPOSITIVO:

  - Físico (cable o wifi necesario para conexión ADB)


  - Emulador  

    https://www.genymotion.com/

    ![](https://github.com/pollonegro/polloFrida/blob/master/img/emulator.png)


- REQUERIMIENTOS DE SOFTWARE :

  - “root” + Paquete de traducción ARM-x86 para Genymotion

  - Burpsuite y certificado.
  
  - Frida:
    
    A. Instalación de las herramientas CLI de Frida: “pip install frida-tools”

    B. Configurar su dispositivo Android:
    
      - Activar depuración USB
      
      - Descargar frida-server (https://github.com/frida/frida/releases)
      
        ![](https://github.com/pollonegro/polloFrida/blob/master/img/frida-server-dw.png)
        
      
      - Descomprimir, instalar en dispositivo, dar permisos y ejecutar.
      
        ![](https://github.com/pollonegro/polloFrida/blob/master/img/frida-server-up.png)
        
        ![](https://github.com/pollonegro/polloFrida/blob/master/img/frida-adbshell.pngg)
        
        ![](https://github.com/pollonegro/polloFrida/blob/master/img/frida-start.png)

  
  
2. Obtención de la APK: Desde el dispositivo (recomendado)

   "adb devices"
   
   "adb shell pm list packages -l"
   
   "adb pull /System/app/BeamService.apk"
   
 











