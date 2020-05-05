# polloFrida
Now.. Hacking with Frida Powers!



-- LABORATORIO ANDROID 8.0 --



- EMULADOR: 

   ![](https://www.genymotion.com/wp-content/themes/genymobile/img/genymobile-with-motion.svg)

    https://www.genymotion.com/download/



- SOFTWARE :

  - Genymotion ARM Translation 
  
  https://github.com/m9rco/Genymotion_ARM_Translation/blob/master/package/Genymotion-ARM-Translation_for_8.0.zip


  - Xposed Android 8.0
  
  https://forum.xda-developers.com/attachment.php?attachmentid=4393082&d=1516301692


  - Burpsuite
  
  https://portswigger.net/burp
  
  
  - Inspeckage 
  
  https://github.com/ac-pm/Inspeckage/releases/download/v2.4/app-release.apk
  
  
  - Frida 
  
  https://github.com/frida/frida/releases/download/12.8.20/frida-server-12.8.20-android-x86.xz
    
    
-----------------------------------------------------------------------------------------------------


- INSTALACION:

    1. Ejecutar Genymotion, arrastrar "Genymotion ARM Translation" al interior, flasherar y reiniciar.
    
    ![](https://github.com/pollonegro/polloFrida/blob/master/img/armgeny.png)
    
    
    2. Arrastrar "XposedInstaller_3.1.5.apk" y "Inspeckage2.4.apk" al interior de Genymotion para su instalacion.
      
    
    3. Instalación de Frida: 
   
      A. Equipo (python & pip requerido)
      
          “pip install frida-tools”


      B. Emulador:
    
        1 Descomprimir, alojar en dispositivo, dar permisos y ejecutar. (renombrado a "frida-server")
        
          adb push ./frida-server /data/local/tmp/
          adb shell 'su -c setenforce 0' 
          adb shell 'su -c /data/local/tmp/frida-server &' 

          ![](https://github.com/pollonegro/polloFrida/blob/master/img/frida-server-up.png)

          ![](https://github.com/pollonegro/polloFrida/blob/master/img/frida-adbshell.pngg)

          ![](https://github.com/pollonegro/polloFrida/blob/master/img/frida-start.png)
          
          
         2 Configurar Xposed 
          
          Activar "Inspeckage" y "TrustMeAlready" en la pestaña modulos y reniciar

  



frida-ps -U 
 
