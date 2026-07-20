# Execute Multiple Requests with Resco Cloud

Executes multiple data operations in Resco Cloud.

## Endpoint

- **Method:** `POST`
- **Path:** `/ExecuteMultiple`
- **Base URL:** `https://{organization}.app.resco.net/rest/v1/data`
- **API:** rest
- **Official documentation:** [Execute Multiple Requests](https://docs.resco.net/wiki/Resco_CRM_Connector)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `rawBody` | body | `string` | yes | XML requests body for the Resco ExecuteMultiple request. |
