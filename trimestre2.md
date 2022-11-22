# Visual Basic 
uso del input box y condicional if 
Eliminar la configuración de proxy en la configuración de Git
7 MAR 2018
Hace ya varios meses había configurado a git para que se conectara usando un proxy de la siguiente forma:

git config --global http.proxy http://mydomain\\myusername:mypassword@myproxyserver:8080

Ahora el cliente ha sacado ese servidor del proxy de tal forma que ya no es necesario por lo tanto falla la conexión al no encontrarlo.

Verificamos la configuración actual con

git config --global -l

Para eliminar esa configuración lo podemos hacer con este comando.

git config --global --unset http.proxy

Luego podemos verificar que efectivamente no esté usando:

git config --global -l
# otros
$git config --global --list
me da:

bash">user.name=test user
user.name=gotqn
Quiero eliminar el nombre. Me refiero a esto artículo y hacer los siguientes comandos pero sin ningún resultado:

git config --global --remove-section user.name='test user'
git config --global --remove-section user.name="test user"
git config --global --remove-section user.name=test user
git config --global --remove-section user.name
git config --global --remove-section test user
Estoy usando ubuntu 12.04 y

git version
me da

git version 1.7.9.5
Por favor, ayuda en esto, porque quiero intentar guardar mi proyecto usando git, pero no quiero ejecutar el comando con nombre de 'usuario de prueba'.



Fuente: https://www.enmimaquinafunciona.com/pregunta/25385/archivo-global-git-config---eliminar-la-configuracion

link 
https://www.mclibre.org/consultar/informatica/lecciones/vsc-git-repositorio.html