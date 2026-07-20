# Create a manual account with Lunch Money

## Endpoint

- **Method:** `POST`
- **Path:** `/manual_accounts`
- **Base URL:** `https://api.lunchmoney.dev/v2`
- **Official documentation:** [Create a manual account](https://alpha.lunchmoney.dev/v2/docs)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `name` | body | `string` | yes |
| `display_name` | body | `string` | no |
| `type` | body | `string` | yes |
| `balance` | body | `number` | yes |
