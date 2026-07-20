# List Templates with Yousign

Retrieves templates from Yousign.

## Endpoint

- **Method:** `GET`
- **Path:** `/templates`
- **Base URL:** `https://api-sandbox.yousign.app/v3`
- **Official documentation:** [List Templates](https://developers.yousign.com/reference/get-templates-1)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `after` | query | `string` | no | Return templates after this pagination cursor. |
| `limit` | query | `number` | no | Maximum number of templates to return. |
