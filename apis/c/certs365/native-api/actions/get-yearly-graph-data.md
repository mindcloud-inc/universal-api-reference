# Get Yearly Graph Data with Certs 365

Retrieves yearly issuer graph data from Certs 365.

## Endpoint

- **Method:** `GET`
- **Path:** `/api/get-graph-data/{year}/{email}`
- **Base URL:** `https://api1.certs365.io`
- **Official documentation:** [Get Yearly Graph Data](https://help.certs365.io/documentation/fetching-upload-request-details/get-graph-endpoints-of-issuer-based-on-the-input-year/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `year` | path | `number` | yes | Year to retrieve graph data for. |
| `email` | path | `string` | yes | Issuer email address. |
