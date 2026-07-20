# Create Group with SimpleKPI

Creates a new group in SimpleKPI.

## Endpoint

- **Method:** `POST`
- **Path:** `groups`
- **Base URL:** `https://{subdomain}.simplekpi.com/api/`
- **Official documentation:** [Create Group](https://support.simplekpi.com/Developers/Groups)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `name` | body | `string` | no | The group name. |
| `sort_order` | body | `number` | no | The display sort order for the group. |
