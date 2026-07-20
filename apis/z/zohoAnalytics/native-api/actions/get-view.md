# Get View with Zoho Analytics

Retrieves a view from Zoho Analytics by ID.

## Endpoint

- **Method:** `GET`
- **Path:** `/views/[:view-id]`
- **Base URL:** `https://analyticsapi.zoho.com/restapi/v2`
- **Official documentation:** [Get View](https://raw.githubusercontent.com/zoho/analytics-oas/main/v2.0/metadata-api.json)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `CONFIG` | query | `string` | no | Optional JSON configuration string such as {"withInvolvedMetaInfo":true}. |
| `view-id` | path | `string` | yes | ID of the view to inspect. |
