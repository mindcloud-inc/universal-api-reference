# Create Group with Go4Clients

Creates a new contact group in Go4Clients.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/groupscontacts/groups/v1.0/`
- **Base URL:** `https://cloud.go4clients.com:8580`
- **Official documentation:** [Create Group](https://apidoc.go4clients.com/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `groupName` | body | `string` | yes | Name of the group to create. |
| `filterParameters[]` | body | `array<object>` | yes | Array of filter objects with key, type, and value. |
