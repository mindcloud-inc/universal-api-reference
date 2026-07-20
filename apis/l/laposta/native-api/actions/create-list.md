# Create List with Laposta

Creates a new list in Laposta.

## Endpoint

- **Method:** `POST`
- **Path:** `/list`
- **Base URL:** `https://api.laposta.nl/v2`
- **Official documentation:** [Create List](https://api.laposta.nl/doc/index.en.php#lists)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `name` | body | `string` | yes | Name of the list to create. |
| `locked` | body | `boolean` | no | Whether the list is locked from user edits. |
| `remarks` | body | `string` | no | Optional remarks for the list. |
| `subscribe_notification_email` | body | `string` | no | Email address notified on new subscriptions. |
| `unsubscribe_notification_email` | body | `string` | no | Email address notified on unsubscribes. |
