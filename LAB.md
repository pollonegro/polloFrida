
-- PREPARACION LABORATORIO ANDROID 8.0 --



- EMULADOR: 

    ![](https://github.com/pollonegro/polloFrida/blob/master/img/genylogo.png)

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
    
    


- INSTALACION:

   A. Ejecutar Genymotion, arrastrar "Genymotion ARM Translation" al interior, flasherar y reiniciar.
    
    ![](https://github.com/pollonegro/polloFrida/blob/master/img/armgeny.png)
    
    
   B. Arrastrar "XposedInstaller_3.1.5.apk" y "Inspeckage2.4.apk" al interior de Genymotion para su instalacion.
      
    
   C. Instalación de Frida: 
   
     - Equipo (python & pip requerido)
      
         “pip install frida-tools”


     - Emulador:
    
     1. Descomprimir, alojar en dispositivo, dar permisos y ejecutar. (renombrado a "frida-server")
        
            adb push ./frida-server /data/local/tmp/
            adb shell 'chmod 755 /data/local/tmp/frida-server' 
            adb shell 'su -c setenforce 0' 
            adb shell 'su -c /data/local/tmp/frida-server &' 
          
          
     2. Configurar Xposed 
          
     - Ejecutar aplicacion e instalar Xposed Framework.  
           
     ![](https://github.com/pollonegro/polloFrida/blob/master/img/xposedd.png)
           
          
     - Activar "Inspeckage" y "TrustMeAlready" en la pestaña modulos y reniciar

     ![](https://github.com/pollonegro/polloFrida/blob/master/img/moduless.png)
           
     - Configuracion de proxy

     ![](https://github.com/pollonegro/polloFrida/blob/master/img/proxy-config.png)
          
          
     - Verificacion
           
           frida -U APLICACION

