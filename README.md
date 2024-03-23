# prestamo-lider

Este formulario está hecho con VUE.
Lo que hace es realizar una petición a un middleware, y el middleware envía la info a un server final.

![Captura de Pantalla 2024-03-23 a la(s) 21 10 07](https://github.com/tanometro/prestamo-lider/assets/53281025/8cd6cc57-6478-4845-8374-bdf07901573c)

Esto es así por el hecho de que WordPress no envía peticiones a servidores que no tengan HTTPS, entonces se utiliza el middleware (más abajo credenciales de middleware).

Lo que se requiere es que haga una petición SOAP acá: http://plider.dyndns.info:8080/RiesgoHook1_plider_WS.aspx?WSDL
Esta api recibe las mismas variables que hoy envian por parámetro en la URL.
![WhatsApp Image 2024-03-12 at 12 48 00 AM](https://github.com/tanometro/prestamo-lider/assets/53281025/64254860-8133-44c2-ae80-bb21ee471c8e)

A continuación screen donde el campo marcado de rojo es la respuesta, vienen dos valores entre [][]
![WhatsApp Image 2024-03-12 at 1 46 53 AM](https://github.com/tanometro/prestamo-lider/assets/53281025/a8ada40b-9e1a-451f-a4b3-d66b46eae621)

El primer valor dice si está rechazado, osea que una N como vino en este caso es que no está rechazado. El valor en el segundo array es que tipo de aprobación tiene, pero eso no le des bola.
Esta seria un caso como el de arriba, no está rechazado, pero ademas aca en P_REN hay un valor mayor que cero.

![WhatsApp Image 2024-03-12 at 1 59 20 AM](https://github.com/tanometro/prestamo-lider/assets/53281025/3411ed7c-24f7-4ff2-8f53-596eff574cc0)

Eso significa que hay planes preaprobados, que aparecen mas abajo, estos planes son los que el cliente puede tomar, aun no se si van a decirle esto al cliente en este momento
Aparecen mas abajo los planes, son muchos, supongo le van a decir el primero que es el mas alto.

![WhatsApp Image 2024-03-12 at 2 00 17 AM](https://github.com/tanometro/prestamo-lider/assets/53281025/30504f4c-b11a-4e03-adac-0660c5d12dc8)

Y este seria un rechazado automático:
![WhatsApp Image 2024-03-12 at 2 03 00 AM](https://github.com/tanometro/prestamo-lider/assets/53281025/6dd4552b-65ee-4370-b287-5e07bd90a0a4)

Ahora bien, lo que se requiere:
A los que NO tengan posibilidad de un prestamo le debería aparecer:
"Por el momento no calificas para un crédito, podes consultar más adelante"
y a los que sí, el mensaje que ya aparece actualmente, "Completaste exitosamente.. etc etc".

Middleware:
En hostimger.com
vilmaefonceca@hotmail.com
17Febrero*

siito web: prestamolider.com -> administrar -> administrador de archivos -> public_html -> proxy

