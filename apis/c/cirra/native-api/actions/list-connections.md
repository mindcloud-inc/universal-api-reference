# List Connections with Cirra

Retrieves Cirra connections for the authenticated user.

## Endpoint

- **Method:** `GET`
- **Path:** `/v1/cirra/connections`
- **Base URL:** `http://api-public:9801`

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `appId` | query | `string` | no | Optional app ID to filter connections by app. |
