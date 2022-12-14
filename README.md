# Analizador semántico 
Este proyecto fue realizado en el lenguage de programación Python, utilizando la versión 3.10 y empleando el entorno de Visual Studio Code para su desarrollo. No obstante, se trabajó a modo de consola e interfaz (utilizando la librería de Pyside2 del entorno QT), realizando esta compactación hibrida para un mejor manejo de la información procesada.

## Instalación
### 1ra forma.
Dar clic en Code, luego en Donwload ZIP y después de que termine la descarga, descomprimirlo.

### 2da forma.
Crear una carpeta, ingresar a git bash y ejecutar el siguiente comando:  git clone https://github.com/OTG-16/Analizador_Semantico.git

### Nota
Es importante resaltar que en este proyecto se utilizan herramientas que deben ser instaladas previamente para el correcto funcionamiento de este analizador. Entre ellas están las siguientes:

- IDE QT Creator
- Librería Pyside2 (Se podría consultar el siguiente video para su instalación https://www.youtube.com/watch?v=INSimE1tW34&list=PLNN_J-C1-lZvgVgnoYXeZo49Boz6CDGTf&index=4 y este otro como introducción para su manejo https://www.youtube.com/watch?v=T0qJdF1fMqo&list=PLNN_J-C1-lZvgVgnoYXeZo49Boz6CDGTf&index=5&t=1533s)
- Librería Colorama (Utlizar en el cmd el comando: pip install colorama)
- Librería Matplotlib (Utlizar en el cmd el comando: pip install matplotlib)
- Librería Networkx (Utlizar en el cmd el comando: pip install networkx)

## Probando el programa
En un principio, al momento de correr el programa este muestra lo siguiente:
#### Interfaz principal
![c1](https://user-images.githubusercontent.com/70919055/191636160-03a7d676-64d0-44b7-be3e-5f74b06b9f8a.PNG)

Puede apreciarse una interfaz. Al lado izquierdo se cuenta con un cuadro de texto (ignorar el de la derecha) para ingresar la información a analizar. En la parte de a medias se tiene un botón, este se usa para comenzar el análisis léxico, sintáctico y semántico. 

Ahora bien, se ingresa en el cuadro correspondiente, el texto 
"int main(){
float a;
int b;
int c;
c = a+b;
c = suma(8,9);
}" 
,ya que se sugirió como primer ejemplo y se da click en el botón de analizar. Al ser una cadena inválida semánticamente el programa muestra una ventana con el mensaje del error, tal como se muestra a continuación:
#### Texto ingresado
![E1](https://user-images.githubusercontent.com/70919055/201827019-2de07252-0b88-419d-8479-feeb5e4a0074.png)
#### Resultado
![E1_2](https://user-images.githubusercontent.com/70919055/201827111-d560b2fa-6582-42b9-9c8d-5b545de92418.png)

No obstante, como segunda prueba se e ingresa en el cuadro correspondiente, el texto
"int a;
int suma(int a, int b){
return a+b;
}

int main(){
float a;
int b;
int c;
c = a+b;
c = suma(8.5,9.9);
}"
,ya que se sugirió como segundo ejemplo y se da click en el botón de analizar. Al ser también una cadena inválida semánticamente el programa muestra una ventana con el mensaje del error, tal como se muestra a continuación:
#### Texto ingresado
![E2](https://user-images.githubusercontent.com/70919055/201827451-47eddeaf-47dd-4d5e-84f3-eda1ec214058.png)
#### Resultado
![E2_2](https://user-images.githubusercontent.com/70919055/201827502-a5e0b5a4-76a3-463d-801a-0a8ed5cb78f8.png)
