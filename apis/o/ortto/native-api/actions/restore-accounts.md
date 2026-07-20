# Restore Accounts with Ortto

## Endpoint

- **Method:** `PUT`
- **Path:** `/accounts/restore`
- **Base URL:** `{apiBaseUrl}/v1`
- **Official documentation:** [Restore Accounts](https://help.ortto.com/a-279-archive-restore-and-delete-organizations-archive-restore-delete)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `inclusion_ids[]` | body | `array<string>` | yes | Account IDs to restore. |
