# Erase from the unsubscribed list with Routee

Deletes entries from the unsubscribed list in Routee.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/smtp/unsubscribe`
- **Base URL:** `https://connect.routee.net`
- **Official documentation:** [Erase from the unsubscribed list](https://docs.routee.net/reference/erasing-from-the-unsubscribed-list)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `emails` | body | `string` | no | A serialized email array |
