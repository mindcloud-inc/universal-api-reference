# Get References with BKK Futar

Retrieves ID-based references from BKK Futar.

## Endpoint

- **Method:** `GET`
- **Path:** `/references.json`
- **Base URL:** `https://futar.bkk.hu/api/query/v1/ws/otp/api/where`
- **Official documentation:** [Get References](https://learn.microsoft.com/en-us/connectors/bkkfutarip/#get-references)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `agencyId` | query | `string` | no | Agency ID to resolve, such as BKK. |
| `alertId` | query | `string` | no | Alert ID to resolve. |
| `routeId` | query | `string` | no | Route ID to resolve. |
| `stopId` | query | `string` | no | Stop ID to resolve, such as BKK_F01227. |
| `includeReferences` | query | `string` | no | Reference data to include in the response. |
