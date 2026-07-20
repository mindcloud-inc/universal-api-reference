# Delete Snapshot with Calibre

Deletes an existing snapshot from Calibre.

## Endpoint

- **Method:** `POST`
- **Path:** `/graphql`
- **Base URL:** `https://api.calibreapp.com`
- **Official documentation:** [Delete Snapshot](https://calibreapp.com/docs/automation/snapshots#delete-a-snapshot)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `variables.site` | body | `string` | yes | Site slug, found in site settings. |
| `variables.iid` | body | `string` | yes | Snapshot IID to delete. |
