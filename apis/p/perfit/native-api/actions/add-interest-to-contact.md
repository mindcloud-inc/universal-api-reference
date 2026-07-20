# Add Interest To Contact with Perfit

## Endpoint

- **Method:** `PUT`
- **Path:** `/:account/contacts/:contactId/interests/:interest`
- **Base URL:** `https://api.myperfit.com/v2`
- **Official documentation:** [Add Interest To Contact](https://developers.myperfit.com/contacts-api/usos-mas-frecuentes/agregar-un-interes-a-un-contacto)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `account` | path | `string` | yes | Perfit account name. |
| `contactId` | path | `string` | yes | Contact email or numeric ID. |
| `interest` | path | `string` | yes | Existing Perfit interest ID. |
