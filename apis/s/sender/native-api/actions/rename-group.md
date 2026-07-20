# Rename Group with Sender

## Endpoint

- **Method:** `PATCH`
- **Path:** `/groups/:id`
- **Base URL:** `https://api.sender.net/v2`
- **Official documentation:** [Rename Group](https://api.sender.net/groups/update-group/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | Group ID. |
| `title` | body | `string` | no | Provide a different name for this group. |
