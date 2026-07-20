# Delete User with Upnify

Deletes an existing user from Upnify.

## Endpoint

- **Method:** `DELETE`
- **Path:** `v4/catalogos/usuarios/:tkUsuario`
- **Base URL:** `https://api.upnify.com`
- **Official documentation:** [Delete User](https://desarrollo.upnify.com/api-rest/catalogos/#api-Usuarios-DeleteCatalogosUsuariosTkusuario)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `tkUsuario` | path | `string` | yes | El código token que corresponde e identifica a un usuario, el cual se requiere su eliminación.  ¿Dónde obtengo el token? |
| `tkReemplazo` | query | `string` | yes | El código token que corresponde al usuario que servirá como remplazo.  ¿Dónde obtengo el token? |
