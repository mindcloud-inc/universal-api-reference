# Delete Accounts with Ortto

## Endpoint

- **Method:** `DELETE`
- **Path:** `/accounts/delete`
- **Base URL:** `{apiBaseUrl}/v1`
- **Official documentation:** [Delete Accounts](https://help.ortto.com/a-279-archive-restore-and-delete-organizations-archive-restore-delete)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `inclusion_ids[]` | body | `array<string>` | yes | Account IDs to delete. |
