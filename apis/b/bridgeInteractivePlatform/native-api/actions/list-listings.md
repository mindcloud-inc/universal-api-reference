# List listings with Bridge Interactive Platform

Retrieves listing records from Bridge Interactive Platform.

## Endpoint

- **Method:** `GET`
- **Path:** `/:dataset/listings`
- **Base URL:** `https://api.bridgedataoutput.com/api/v2`
- **Official documentation:** [List listings](https://bridgedataoutput.com/docs)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `dataset` | path | `string` | yes | Bridge dataset code. This tenant was validated against dataset test. |
| `fields` | query | `string` | no | Comma-separated response fields to include. |
| `limit` | query | `string` | no | Maximum number of listings to return. |
| `offset` | query | `string` | no | Number of listings to skip before returning results. |
| `order` | query | `string` | no | Sort direction: asc or desc. |
| `sortBy` | query | `string` | no | Response field to sort listings by. |
