# Select Records with Resco Cloud

Retrieves entity records from Resco Cloud.

## Endpoint

- **Method:** `GET`
- **Path:** `/:entity`
- **Base URL:** `https://{organization}.app.resco.net/rest/v1/data`
- **API:** rest
- **Official documentation:** [Select Records](https://docs.resco.net/wiki/Resco_CRM_Connector)

## Capabilities

This operation supports [pagination](../README.md#pagination), [filtering](../README.md#filtering), and [sorting](../README.md#sorting).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `entity` | path | `string` | yes | Resco entity logical name, for example account or contact. |
| `$select` | query | `string` | no | Comma-separated attribute names to include in the response. |
| `$filter` | query | `string` | no | Resco filter expression, for example name LIKE 'C%'. |
