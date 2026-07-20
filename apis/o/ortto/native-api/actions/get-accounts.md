# Get Accounts with Ortto

## Endpoint

- **Method:** `POST`
- **Path:** `/accounts/get`
- **Base URL:** `{apiBaseUrl}/v1`
- **Official documentation:** [Get Accounts](https://help.ortto.com/a-277-retrieve-one-or-more-organizations-get)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `fields[]` | body | `array<string>` | yes | Account field IDs to return, such as str::name. |
| `limit` | body | `number` | no | Maximum number of accounts to return. |
| `offset` | body | `number` | no | Number of accounts to skip. |
| `sort_by_field_id` | body | `string` | no | Account field ID to sort by. |
| `sort_order` | body | `string` | no | Sort direction. |
| `q` | body | `string` | no | Search accounts by name. |
