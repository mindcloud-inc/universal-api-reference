# Merge multiple groups with Routee

Merges multiple groups in your Routee account.

## Endpoint

- **Method:** `POST`
- **Path:** `/groups/my/merge`
- **Base URL:** `https://connect.routee.net`
- **Official documentation:** [Merge multiple groups](https://docs.routee.net/reference/merge-multiple-groups)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `name` | body | `string` | yes | The name of the group to be created. Length must be between 2 and 30 characters. |
| `groups` | body | `string` | yes | The names of the groups that will be merged. |
