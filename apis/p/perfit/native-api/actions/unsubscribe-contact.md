# Unsubscribe Contact with Perfit

## Endpoint

- **Method:** `POST`
- **Path:** `/:account/contacts/:contactId/unsubscribe`
- **Base URL:** `https://api.myperfit.com/v2`
- **Official documentation:** [Unsubscribe Contact](https://developers.myperfit.com/contacts-api/usos-mas-frecuentes/desuscribir-a-un-contacto)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `account` | path | `string` | yes | Perfit account name. |
| `contactId` | path | `string` | yes | Contact email or numeric ID. |
