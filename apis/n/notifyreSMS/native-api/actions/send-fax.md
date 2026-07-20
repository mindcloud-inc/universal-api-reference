# Send Fax with Notifyre SMS

Creates a fax message in Notifyre.

## Endpoint

- **Method:** `POST`
- **Path:** `/fax/send`
- **Base URL:** `https://api.notifyre.com/20220711`
- **Official documentation:** [Send Fax](https://docs.notifyre.com/api/fax-send)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `documents` | body | `list<object>` | yes | Documents to upload and send as fax pages. |
| `recipients` | body | `list<object>` | yes | Fax recipients. |
| `sendFrom` | body | `string` | yes | Fax number or sender identifier used to send. |
