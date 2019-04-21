# full stack react django

A. Configurar docker
  1. Crear Dockerfile
  2. Crear docker-compose.yml
  3. Crear requirements.txt
  4. sudo docker-compose run web django-admin startproject leadmanager .
  5. sudo chown -R $USER:$USER .
  6. python3.6 manage.py startapp leads
  7. register app in setting.py
  8. Build models in app
  9. python3.6 makemigrations leads
  10. python3.6 manage.py migrate
  11. create serializers
  12. create viewsets (api.py)
  13. incluir dentro de el archivo url.py del proyecto (leadmanager) la ruta hacía las urls de la app (leads)
  14. configurar las urls de la aplicacion en un nuevo archivo llamado urls.py dentro de la app
  15. sudo docker-compose up => levantar servicio
  16. postman get => http://localhost:8000/api/leads
  17. insert from postman POST
      A. header => Content-Type => application/json
      B. Body => row
          {
            "name": "John Doe",
            "email": "jdoe@gmail.com",
            "message": "Please contact John"
          }
  18. probar el get nuevamente y debería tener un registro
