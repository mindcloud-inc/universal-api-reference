# Split a transaction with Lunch Money

## Endpoint

- **Method:** `POST`
- **Path:** `/transactions/split/:id`
- **Base URL:** `https://api.lunchmoney.dev/v2`
- **Official documentation:** [Split a transaction](https://alpha.lunchmoney.dev/v2/docs)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `id` | path | `number` | yes |
| `child_transactions[]` | body | `array<object>` | yes |
