# Update Record with Resco Cloud

Updates a record in Resco Cloud.

## Endpoint

- **Method:** `POST`
- **Path:** `/Update`
- **Base URL:** `https://{organization}.app.resco.net/rest/v1/data`
- **API:** rest
- **Official documentation:** [Update Record](https://docs.resco.net/wiki/Resco_CRM_Connector)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `rawBody` | body | `string` | yes | XML Entity body for the Resco Update request. |
| `$create` | query | `boolean` | no | When true, Resco creates the record if it does not already exist. |
