# Update Group with Notifyre SMS

Updates an existing group in Notifyre.

## Endpoint

- **Method:** `PUT`
- **Path:** `/addressbook/groups/:groupId`
- **Base URL:** `https://api.notifyre.com/20220711`
- **Official documentation:** [Update Group](https://docs.notifyre.com/api/address-book-group-update)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `groupId` | path | `string` | yes | Group identifier. |
| `name` | body | `string` | yes | Updated group name. |
