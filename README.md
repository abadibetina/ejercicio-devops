###app.py 
levanta una aplicacion web usando flask que devuelve un 'Bienvenido a DevOps'. La aplicacion va a correr adentro de un contenedor docker que se especifica en DOCKERFILE y se va a exponer en el puerto 5000 del contenedor.

###DOCKERFILE
# buildeo la imagen manualmente y la llamo flask-app
docker build -t flask-app . 
# corro la imagen como un contenedor
docker run -p 5000:5000 flask-app


###ci.yml
En este archivo esta configurado para que cada vez que se haga un push, se ejecute un pipeline donde se le pide una maquina virtual a github y se buildea y ejecuta el contenedor, para chequear que este todo en orden.