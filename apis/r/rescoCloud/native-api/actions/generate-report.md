# Generate Report with Resco Cloud

Generates a mobile report in Resco Cloud.

## Endpoint

- **Method:** `POST`
- **Path:** `/GenerateReport`
- **Base URL:** `https://{organization}.app.resco.net/rest/v1/data`
- **API:** rest
- **Official documentation:** [Generate Report](https://docs.resco.net/wiki/Resco_CRM_Connector)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `rawBody` | body | `string` | yes | XML report request body for the Resco GenerateReport request. |
