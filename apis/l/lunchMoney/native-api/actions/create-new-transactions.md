# Create transactions with Lunch Money

## Endpoint

- **Method:** `POST`
- **Path:** `/transactions`
- **Base URL:** `https://api.lunchmoney.dev/v2`
- **Official documentation:** [Create transactions](https://alpha.lunchmoney.dev/v2/docs)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `transactions[]` | body | `array<object>` | yes |
| `apply_rules` | body | `boolean` | no |
| `skip_duplicates` | body | `boolean` | no |
