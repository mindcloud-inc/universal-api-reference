# Fetch Records with Resco Cloud

Retrieves records from Resco Cloud using a Fetch query.

## Endpoint

- **Method:** `POST`
- **Base URL:** `https://{organization}.app.resco.net/rest/v1/data`
- **API:** rest
- **Official documentation:** [Fetch Records](https://docs.resco.net/wiki/Resco_CRM_Connector)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `rawBody` | body | `string` | yes | FetchXML body for the Resco REST request. |
