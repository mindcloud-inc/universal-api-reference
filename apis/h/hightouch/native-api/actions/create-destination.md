# Create Destination with Hightouch

Creates a new destination in Hightouch.

## Endpoint

- **Method:** `POST`
- **Path:** `/destinations`
- **Base URL:** `https://api.hightouch.com/api/v1`
- **Official documentation:** [Create Destination](https://api.hightouch.io/api/swagger.json)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `name` | body | `string` | yes | The destination name. |
| `slug` | body | `string` | yes | The destination slug. |
| `type` | body | `string` | yes | The destination type, such as salesforce or hubspot. |
| `configuration` | body | `object` | yes | Destination configuration object for the selected destination type. |
