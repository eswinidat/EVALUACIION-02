1.	[Saga Ripley] Diseña un caso de prueba de REGRESIÓN para verificar que, tras una actualización del módulo de pagos, el flujo de compra con cupón de descuento sigue funcionando correctamente. Incluye: flujo feliz, flujo alterno (cupón expirado) y flujo de error (fallo en pasarela).

Respuesta:

Usuario registrado
Producto disponible 
Cupo valido = ejemplo (desc 10)
Medio de pago


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
