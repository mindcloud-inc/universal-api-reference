# Delete People with Ortto

## Endpoint

- **Method:** `DELETE`
- **Path:** `/person/delete`
- **Base URL:** `{apiBaseUrl}/v1`
- **Official documentation:** [Delete People](https://help.ortto.com/a-260-archive-restore-and-delete-people-archive-restore-delete)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `inclusion_ids[]` | body | `array<string>` | yes | People IDs to delete. |
