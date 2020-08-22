# Configuration-firebase

## Realtime Database
Es necesario darles permiso para la lectura y escritura 
```Realtime Database->Reglas```

```javascript
{
  "rules": {
    ".read": true,
    ".write": true
  }
}
``` 
Después le damos en publicar

## Storage
Previamente se debe de configurar la zona local.

Para dar los permisos necesarios 

```Storage->Reglas```

```javascript
rules_version = '2';
service firebase.storage {
  match /b/{bucket}/o {
    match /{allPaths=**} {
      allow read, write;
    }
  }
}
``` 
Después le damos en publicar

​
## Authentication
Podemos dar permisos para la authentication 
Ejm.
- Correo electrónico
- Gmail
### Correo electrónico
habilitamos las 2 opciones 

* Permite a los usuarios registrarse con su dirección de correo electrónico y contraseña. 
* Enviar enlace por correo electrónico (inicio de sesión sin contraseña)

### Gmail
Ingresamos nuestro correo y le damos en habilitar 