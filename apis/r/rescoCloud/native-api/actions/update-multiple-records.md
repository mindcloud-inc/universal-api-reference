# Update Multiple Records with Resco Cloud

Updates multiple records in Resco Cloud.

## Endpoint

- **Method:** `POST`
- **Path:** `/UpdateMultiple`
- **Base URL:** `https://{organization}.app.resco.net/rest/v1/data`
- **API:** rest
- **Official documentation:** [Update Multiple Records](https://docs.resco.net/wiki/Resco_CRM_Connector)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `rawBody` | body | `string` | yes | XML Entities body for the Resco UpdateMultiple request. |
| `$create` | query | `boolean` | no | When true, Resco creates records that do not already exist. |
