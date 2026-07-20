# Create Enterprise with Kiwili

Creates a new enterprise in Kiwili.

## Endpoint

- **Method:** `POST`
- **Path:** `/enterprise`
- **Base URL:** `https://mindcloud.kiwili.com/api`
- **Official documentation:** [Create Enterprise](https://api.kiwili.com/api/openapi/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `Email` | body | `string` | no | Primary email address for the enterprise. |
| `IsClient` | body | `boolean` | no | Whether the enterprise is a client. |
| `Name` | body | `string` | yes | The enterprise name. |
