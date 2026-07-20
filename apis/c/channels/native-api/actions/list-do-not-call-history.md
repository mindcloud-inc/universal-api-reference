# List Do Not Call History with Channels

Retrieves do-not-call history from Channels.

## Endpoint

- **Method:** `GET`
- **Path:** `/api/v1/dnclist`
- **Base URL:** `https://api.channels.app`
- **Official documentation:** [List Do Not Call History](https://developers.channels.app/)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `dateFrom` | query | `string` | no | Optional lower bound for Do Not Call List event date. |
| `dateTo` | query | `string` | no | Optional upper bound for Do Not Call List event date. |
| `direction` | query | `string` | no | Optional sort direction for Do Not Call List history. |
| `msisdnLike` | query | `string` | no | Optional phone-number contains filter. |
| `orderColumn` | query | `string` | no | Optional column to order Do Not Call List history by. |
