# Delete Multiple Records with Resco Cloud

Deletes multiple records from Resco Cloud.

## Endpoint

- **Method:** `POST`
- **Path:** `/DeleteMultiple`
- **Base URL:** `https://{organization}.app.resco.net/rest/v1/data`
- **API:** rest
- **Official documentation:** [Delete Multiple Records](https://docs.resco.net/wiki/Resco_CRM_Connector)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `rawBody` | body | `string` | yes | XML Entities body for the Resco DeleteMultiple request. |
