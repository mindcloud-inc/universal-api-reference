# Get Sequence Settings with Saleshandy

## Endpoint

- **Method:** `GET`
- **Path:** `/sequences/[:sequenceId]/settings`
- **Base URL:** `https://open-api.saleshandy.com/v1`
- **Official documentation:** [Get Sequence Settings](https://developer.saleshandy.com/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `sequenceId` | path | `string` | yes | Sequence ID to fetch settings for. |
| `code` | query | `number` | no | Optional settings code to filter the response. |
