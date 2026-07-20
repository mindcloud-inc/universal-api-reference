# Upsert Accounts with Ortto

## Endpoint

- **Method:** `POST`
- **Path:** `/accounts/merge`
- **Base URL:** `{apiBaseUrl}/v1`
- **Official documentation:** [Upsert Accounts](https://help.ortto.com/a-278-create-or-update-one-or-more-organizations-merge)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `accounts[]` | body | `array<object>` | yes | Accounts to create or update. |
| `merge_by[]` | body | `array<string>` | yes | Account fields used to find existing accounts. |
| `async` | body | `boolean` | no | Queue the merge asynchronously. |
| `merge_strategy` | body | `number` | no | How existing account values should be merged. |
| `find_strategy` | body | `number` | no | How merge fields should be used when finding accounts. |
