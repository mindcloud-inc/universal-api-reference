# Delete emails from a mailing list with Routee

Deletes emails from a mailing list in Routee.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/addressbooks/:listId/emails`
- **Base URL:** `https://connect.routee.net`
- **Official documentation:** [Delete emails from a mailing list](https://docs.routee.net/reference/deleting-emails-from-a-mailing-list)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `number` | yes | List ID |
| `list_id` | path | `string` | yes | — |
| `emails[]` | body | `array<string>` | yes | A serialized array of emails |
