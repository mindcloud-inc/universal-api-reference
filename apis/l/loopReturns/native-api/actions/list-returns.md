# List Returns with Loop Returns

Pull a detailed list of returns created within a given timeframe.

## Endpoint

- **Method:** `GET`
- **Path:** `/warehouse/return/list`
- **Base URL:** `https://api.loopreturns.com/api/v1`
- **Official documentation:** [List Returns](https://docs.loopreturns.com/api-reference/latest/return-data/detailed-returns-list)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `state` | query | `list<string>` | no | Only include returns in a particular state. If left blank, the response may include __open__, __closed__, and __expired__ returns.  Available options: `open`, `closed`, `cancelled`, `expired`, `review` |
| `from` | query | `date` | no | — |
| `to` | query | `date` | no | — |
| `filter` | query | `list<string>` | no | The date used to filter results.  Available options: `created_at`, `updated_at` |
