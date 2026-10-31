# Reorder Person Fields with Bridgit Bench

## Endpoint

- **Method:** `PUT`
- **Path:** `/rp/api/v1/accounts/:id/person-fields/_reorder`
- **Base URL:** `https://bench.gobridgit.com`
- **Official documentation:** [Reorder Person Fields](https://developers.gobridgit.com/reference/personfields_updatefieldorder)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `number` | yes | The account ID |
| `payload[]` | body | `array<object>` | yes | — |
| `payload[].fieldId` | body | `number` | yes | The field ID to reorder |
| `payload[].displayOrder` | body | `number` | yes | The new display order position (1-indexed) |
