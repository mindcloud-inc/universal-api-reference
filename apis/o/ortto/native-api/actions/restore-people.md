# Restore People with Ortto

## Endpoint

- **Method:** `PUT`
- **Path:** `/person/restore`
- **Base URL:** `{apiBaseUrl}/v1`
- **Official documentation:** [Restore People](https://help.ortto.com/a-260-archive-restore-and-delete-people-archive-restore-delete)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `inclusion_ids[]` | body | `array<string>` | yes | People IDs to restore. |
