# Create a transaction group with Lunch Money

## Endpoint

- **Method:** `POST`
- **Path:** `/transactions/group`
- **Base URL:** `https://api.lunchmoney.dev/v2`
- **Official documentation:** [Create a transaction group](https://alpha.lunchmoney.dev/v2/docs)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `ids[]` | body | `array<number>` | yes |
| `date` | body | `string` | yes |
| `payee` | body | `string` | yes |
