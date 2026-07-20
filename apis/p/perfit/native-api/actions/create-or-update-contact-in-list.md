# Create Or Update Contact In List with Perfit

## Endpoint

- **Method:** `POST`
- **Path:** `/:account/lists/:list/contacts`
- **Base URL:** `https://api.myperfit.com/v2`
- **Official documentation:** [Create Or Update Contact In List](https://developers.myperfit.com/contacts-api/usos-mas-frecuentes/crear-o-actualizar-un-contacto-en-una-lista)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `account` | path | `string` | yes | Perfit account name. |
| `list` | path | `string` | yes | Perfit list ID. |
| `email` | body | `string` | yes | Contact email address. |
| `firstName` | body | `string` | no | Contact first name. |
| `lastName` | body | `string` | no | Contact last name. |
