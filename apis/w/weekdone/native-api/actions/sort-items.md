# Sort Items with Weekdone

Updates item order for a week in Weekdone.

## Endpoint

- **Method:** `POST`
- **Path:** `item/:itemId/sort`
- **Base URL:** `https://api.weekdone.com/1/`
- **Official documentation:** [Sort Items](https://weekdone.com/developer#h-items)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `itemId` | path | `number` | yes | — |
| `list` | body | `number` | yes | Send multiple values as a string separated by `,`. |
| `period` | body | `string` | yes | — |
| `type_id` | body | `number` | yes | — |
