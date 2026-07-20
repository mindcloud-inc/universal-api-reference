# Search Contacts with EZContact

## Endpoint

- **Method:** `POST`
- **Path:** `/mcp.php`
- **Base URL:** `https://app.ezcontact.ai/api`
- **Official documentation:** [Search Contacts](https://app.ezcontact.ai/docs/API.md)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `params.telefono` | body | `string` | no | Partial phone number to search for. |
| `params.nombre` | body | `string` | no | Partial contact name to search for. |
| `params.limit` | body | `number` | no | Maximum number of contacts to return. |
