# Account Statistics with Scanova

## Endpoint

- **Method:** `GET`
- **Path:** `/auth/stats/`
- **Base URL:** `https://management.scanova.io`
- **Official documentation:** [Account Statistics](https://docs.scanova.io/api-reference/endpoint/analytics/stats)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `fields` | query | `string` | no | Comma-separated list of fields to include in the response. If not specified, all fields are returned. Send multiple values as a string separated by `,`. |
