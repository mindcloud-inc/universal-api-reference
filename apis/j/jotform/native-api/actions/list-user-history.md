# List User History with Jotform

Retrieves user history entries from Jotform.

## Endpoint

- **Method:** `GET`
- **Path:** `/user/history`
- **Base URL:** `https://api.jotform.com`
- **Official documentation:** [List User History](https://api.jotform.com/docs/)

## Capabilities

This operation supports [pagination](../README.md#pagination), [filtering](../README.md#filtering), and [sorting](../README.md#sorting).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `action` | query | `string` | no | Filter history by action type. |
| `date` | query | `string` | no | Filter history by a specific date. |
| `endDate` | query | `string` | no | History end date. |
| `sortBy` | query | `string` | no | Sort history by field. |
| `startDate` | query | `string` | no | History start date. |
