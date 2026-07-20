# Get User with Upnify

Retrieves a user from Upnify.

## Endpoint

- **Method:** `GET`
- **Path:** `v4/catalogos/usuarios/:tkUsuario`
- **Base URL:** `https://api.upnify.com`
- **Official documentation:** [Get User](https://desarrollo.upnify.com/api-rest/catalogos/#api-Usuarios-GetCatalogosUsuariosTkusuario)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `tkUsuario` | path | `string` | yes | Código token que corresponde e identifica de forma única a un usuario en el sistema, del cual se requiere obtener los detalles.  ¿Dónde obtengo el token? |
