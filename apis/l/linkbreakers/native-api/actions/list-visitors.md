# List Visitors with Linkbreakers

Retrieves a list of visitors from Linkbreakers.

## Endpoint

- **Method:** `GET`
- **Path:** `/v1/visitors`
- **Base URL:** `https://api.linkbreakers.com`
- **Official documentation:** [List Visitors](https://linkbreakers.com/help/api/visitors)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `email` | query | `string` | no | Exact-match email filter. |
| `search` | query | `string` | no | Fuzzy search across visitor fields. |
| `include[]` | query | `array<string>` | no | Relationships to include in the response. |
| `linkId` | query | `string` | no | Filter visitors by link ID. |
| `responseFormat` | query | `string` | no | Desired response format. |
