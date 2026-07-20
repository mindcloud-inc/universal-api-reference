# Get Status Graph Data with Certs 365

Retrieves monthly status graph data from Certs 365.

## Endpoint

- **Method:** `GET`
- **Path:** `/api/get-status-graph-data/{month}/{year}/{email}`
- **Base URL:** `https://api1.certs365.io`
- **Official documentation:** [Get Status Graph Data](https://help.certs365.io/documentation/fetching-upload-request-details/get-graph-endpoints-features-of-the-issuer-based-on-month-year/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `month` | path | `number` | yes | Month to retrieve status graph data for. |
| `year` | path | `number` | yes | Year to retrieve status graph data for. |
| `email` | path | `string` | yes | Issuer email address. |
