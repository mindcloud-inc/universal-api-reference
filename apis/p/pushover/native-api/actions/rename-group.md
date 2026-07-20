# Rename Group with Pushover

## Endpoint

- **Method:** `POST`
- **Path:** `/groups/:group/rename.json`
- **Base URL:** `https://api.pushover.net/1`
- **Official documentation:** [Rename Group](https://pushover.net/api/groups#rename)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `group` | path | `string` | yes | Key of the group to rename. |
| `name` | query | `string` | yes | New name for the group. |
