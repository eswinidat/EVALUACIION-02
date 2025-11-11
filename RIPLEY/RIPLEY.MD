1.	[Saga Ripley] Diseña un caso de prueba de REGRESIÓN para verificar que, tras una actualización del módulo de pagos, el flujo de compra con cupón de descuento sigue funcionando correctamente. Incluye: flujo feliz, flujo alterno (cupón expirado) y flujo de error (fallo en pasarela).

Respuesta:

Usuario registrado
Producto disponible 
Cupo valido = ejemplo (desc 10)
Medio de pago

descripcion: el cupón de descuento válido se aplica correctamente y la compra se completa exitosamente.

Campo	Detalle
ID	RIPLEY-01
TIPO 	REGRESION
PRECONDICIONES	USUARIO LOGUEADO, CUPON VALIDO

EL USUARIO INGRESA A LA PAGINA DE RIPLEY.COM
SELECCIONAR UN PRODUCTO DISPONIBLE
AÑADIR AL CARRITO
IR A PAGAR
INGRESAR EL CUPO DE DESCUENTO QUE ES 10%
CONFIRMA EL PAGO CON VISA 

RESULTADO ESPERADO : EL DECUENTO SE APLICA CORRECTAMENTE Y COMPRA EXITOSA   PAGO FINAL DESCONTADO
EVIDENCIA : CAPTURA DE  PANTALLA DE COMPRA EXITOSA

------------------------------------------------------------------------------


FLUJO ALTERNO
Campo	Detalle
ID	RIPLEY-02
PRECONDICIONES	USUARIO LOGUEADO, CUPON VALIDO

descrpcion : el sistema no realiza el descuento y muestra un mensaje indicando que el cupón no es válido o está expirado.
PASOS
EL USUARIO INGRESA CUPO AXPIRAD0

RESULTADO ESPERADO : EL SISTEMA ARROJA UN MENSAJE : CUPO AXPIRADO Y NO VALIDO

EVIDENCIA :CAPTURA DE ERROR MOSTRADO


-------------------------------------------------------------------------------------------



FLUJO DE ERROR
Campo	Detalle
ID	RIPLEY-03
PRECONDICIONES	TARJETA RECHAZADA


descripcion: Comprobar que, si ocurre un error durante el proceso de pago tarjeta rechazada  el sistema muestra un mensaje de fallo y no procesa la compra.

PASOS:
SELECCIONAR UN PRODUCTO
AGREGAR EL CUPO DE DESCUENTO
 
PAGAR CON TARJETA RECXHAZDA

RESULTADO ESPERADO: PAGO RECHAZADO , INTENTE NUEVAMENTE

EVIUDENCIA: CAPTURA DEL ERROR AL COMPRA EL PRODUCTO

