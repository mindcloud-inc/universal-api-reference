# Get Connection with Universal API

Retrieves a connection from Universal API.

## Endpoint

- **Method:** `GET`
- **Path:** `/api/connections/{universalApi}/{serviceId}`
- **Base URL:** `https://api.prod.universalapi.io`
- **Official documentation:** [Get Connection](https://docs.universalapi.io/reference/get-connection)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `universalApi` | path | `string` | yes | Unified API key such as hris, mdm, or distributors. |
| `serviceId` | path | `string` | yes | Connected service identifier. |
