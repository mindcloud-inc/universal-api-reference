# Query Custom Objects with LoginRadius

Retrieves custom object records from LoginRadius by query.

## Endpoint

- **Method:** `POST`
- **Path:** `https://cloud-api.loginradius.com/customobject`
- **Base URL:** `https://api.loginradius.com`
- **Official documentation:** [Query Custom Objects](https://www.loginradius.com/docs/api/openapi/get-all-custom-objects-by-query/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `customobject` | query | `string` | yes | Name of the custom object. |
| `region` | query | `string` | no | Region filter for the results. |
| `from` | body | `date` | no | Start date for the custom object query range. |
| `to` | body | `date` | no | End date for the custom object query range. |
| `size` | body | `number` | no | Maximum number of records to return. |
