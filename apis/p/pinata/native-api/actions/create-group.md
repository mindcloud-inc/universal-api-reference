# Create Group with Pinata

Creates a new group in Pinata.

## Endpoint

- **Method:** `POST`
- **Path:** `/v3/groups/:network`
- **Base URL:** `https://api.pinata.cloud`
- **Official documentation:** [Create Group](https://docs.pinata.cloud/api-reference/endpoint/create-group)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `name` | body | `string` | yes | Name of the group to create. |
| `network` | path | `string` | yes | Target network (`public` or `private`). |
