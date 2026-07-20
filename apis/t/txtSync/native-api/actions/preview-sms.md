# Preview SMS with TxtSync

Previews an SMS message in TxtSync.

## Endpoint

- **Method:** `POST`
- **Path:** `/sms/preview`
- **Base URL:** `https://api.txtsync.com`
- **Official documentation:** [Preview SMS](https://docs.txtsync.com/#preview-sms)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `To` | body | `string` | no | — |
| `ToContactID` | body | `list<number>` | no | Send multiple values as a array. |
| `ToTagID` | body | `list<number>` | no | Send multiple values as a array. |
| `Message` | body | `string` | yes | — |
| `Index` | body | `number` | yes | — |
