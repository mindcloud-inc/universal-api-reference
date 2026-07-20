# Send Single SMS with TxtSync

Creates a single SMS message in TxtSync.

## Endpoint

- **Method:** `POST`
- **Path:** `/sms/send`
- **Base URL:** `https://api.txtsync.com`
- **Official documentation:** [Send Single SMS](https://docs.txtsync.com/#send-single-sms)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `From` | body | `string` | no |
| `To` | body | `string` | no |
| `ToContactID` | body | `number` | no |
| `Message` | body | `string` | yes |
