# List Letters with Postbode

Retrieves letters from a specific Postbode mailbox.

## Endpoint

- **Method:** `GET`
- **Path:** `/mailbox/:mailbox_id/letters`
- **Base URL:** `https://app.postbode.nu/api`
- **Official documentation:** [List Letters](https://github.com/postbode/postbode-api#list-all-letters-in-mailbox)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `mailbox_id` | path | `number` | yes | The Postbode mailbox ID. |
