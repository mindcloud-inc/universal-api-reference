# Update Contact with Perfit

## Endpoint

- **Method:** `PUT`
- **Path:** `/:account/contacts/:contactId`
- **Base URL:** `https://api.myperfit.com/v2`
- **Official documentation:** [Update Contact](https://developers.myperfit.com/contacts-api/usos-mas-frecuentes/modificar-un-contacto-existente)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `account` | path | `string` | yes | Perfit account name. |
| `contactId` | path | `string` | yes | Contact email or numeric ID. |
| `firstName` | body | `string` | no | Updated first name. |
| `lastName` | body | `string` | no | Updated last name. |
