# List Client Folders with noCRM.io

Retrieves client folders from noCRM.io.

## Endpoint

- **Method:** `GET`
- **Path:** `/clients`
- **Base URL:** `{baseUrl}/api/v2`
- **Official documentation:** [List Client Folders](https://www.nocrm.io/api#list-the-client-folders)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `direction` | query | `string` | no | Sort direction for returned client folders. |
| `order` | query | `string` | no | Sort client folders by name or id. |
