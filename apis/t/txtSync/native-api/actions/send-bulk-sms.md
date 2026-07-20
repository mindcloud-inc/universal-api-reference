# Send Bulk SMS with TxtSync

Creates bulk SMS messages in TxtSync.

## Endpoint

- **Method:** `POST`
- **Path:** `/sms/bulk`
- **Base URL:** `https://api.txtsync.com`
- **Official documentation:** [Send Bulk SMS](https://docs.txtsync.com/#send-bulk-sms)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `From` | body | `string` | yes | — |
| `To` | body | `list<string>` | no | Send multiple values as a array. |
| `ToContactID` | body | `list<number>` | no | Send multiple values as a array. |
| `ToTagID` | body | `list<number>` | no | Send multiple values as a array. |
| `Message` | body | `string` | yes | — |
