# Get Letter with Postbode

Retrieves a letter from a specific Postbode mailbox.

## Endpoint

- **Method:** `GET`
- **Path:** `/mailbox/:mailbox_id/letter/:letter_id`
- **Base URL:** `https://app.postbode.nu/api`
- **Official documentation:** [Get Letter](https://github.com/postbode/postbode-api#list-all-letters-in-mailbox)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `mailbox_id` | path | `number` | yes | The Postbode mailbox ID. |
| `letter_id` | path | `number` | yes | The Postbode letter ID. |
