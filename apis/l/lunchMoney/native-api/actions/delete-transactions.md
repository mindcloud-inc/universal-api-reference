# Bulk delete existing transactions with Lunch Money

## Endpoint

- **Method:** `DELETE`
- **Path:** `/transactions`
- **Base URL:** `https://api.lunchmoney.dev/v2`
- **Official documentation:** [Bulk delete existing transactions](https://alpha.lunchmoney.dev/v2/docs)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `ids[]` | body | `array<number>` | yes |
