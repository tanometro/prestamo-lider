# prestamo-lider

Anteriormente, el formulario tenía los campos que ya tiene, inclusive un campo CODIGO DE ÁREA y otro NUMERO DE TELEFONO; solo que para algunos clientes, el navegador les mostraba el codigo postal, por lo que mandaba a la api 3300 - {numero de telefono} en vez de 3764 - {numero de telefono}.

Yo en una tarde muy inspirado, eliminé el campo CODIGO DE AREA y a la m*****, pero ahora la api envía así:
code_area: 0 
telefono: 3764516377

Entonces, lo que se necesita es que esté el campo codigo de área (eso puedo hacerlo yo en el HTML) pero que el navegador no muestre codigo postal ni nada, que el cliente ponga lo que se le de la gana;

ESTIMO que al no haber tocado nada de la api ni de los datos, al ponerle el campo de nuevo debería seguir funcionando correctamente; pero que no muestre codigo postal.
