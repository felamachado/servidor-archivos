# servidor-archivos
Simple y básico servidor web de archivos con Docker-compose y Nginx.

# Instalación

   * Ejecutar el yml con docker-compose.
          
          ```
          docker-compose -f servidor-web.yml up -d
          ```
          
   * Entrar en el docker
          
          ```
          docker exec -i -t nginx-webserver /bin/bash
          ```
          
   * Editar el archivo /etc/nginx/conf.d/default.conf y agregar la linea  ```autoindex on``` en el bloque location:
            
            ```
            location / {
              root   /usr/share/nginx/html;
              autoindex on;
            }
            ```
            
- La carpeta en root, debe ser la misma que en el yml.
