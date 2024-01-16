## Modelo de Consultas

### Registro usuario:
db.createUser({ "usuario": "nombre", "contraseña": "123456789", "email": "correo@ejemplo.com"});

### Registrar nuevo transportista:
db.createTransportUser({ "usuario": "nombre", "contraseña": "123456789", "email": "correo@ejemplo.com"});

### Revisar si el usuario existe en la base de datos:
db.usuario.find({"nombre": "Pablo", "email": "correo@ejemplo.com"});

### Ejemplo con cambio de email:
db.usuario.update({ "email": "correo@ejemplo.com"}, { ¢set: { "email": "nuevo_correo@ejemplo.com});


### Revisar si el transportista está disponible:
db.transportista.find ({ "disponibilidad": "Disponible"});


### Saber si el posicionamiento del transportista es bueno o malo[]():
db.transportista.find ({ "posicionamiento": "Bueno"});

### Revisar el volumen de la mercancía:
db.mercancia.findOne({ "id_mercancia": "numero_ID" }, { "volumen": 1 });

### Revisar si el pago se ha efectuado:
db.pago.find({ "orderId": "numero_orden"}, { "status": 1, "pago.bizum" : 1}); 


### Bloquear en la app al transportista en servicio una vez se haya efectuado el pago de la orden:
db.transportista.update ({ "transportistaId": "ID_transportista}, { ¢set { "estado": "No disponible"}});]()