# Edit a mailing list with Routee

Updates a mailing list in Routee.

## Endpoint

- **Method:** `PUT`
- **Path:** `/addressbooks/:id`
- **Base URL:** `https://connect.routee.net`
- **Official documentation:** [Edit a mailing list](https://docs.routee.net/reference/editing-a-mailing-list)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | the ID of the mailing list |
| `name` | body | `string` | yes | The new name of the mailing list |
