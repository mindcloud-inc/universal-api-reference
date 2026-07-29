# List ERPs with Rillion Prime Web Service

List the ERP systems configured in Rillion Prime.

## Endpoint

- **Method:** `POST`
- **Base URL:** `{baseUrl}`

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `ERP` | body | `string` | no | ERP identifier to filter by. |
| `Primary` | body | `boolean` | no | When true, only return the primary ERP. |
