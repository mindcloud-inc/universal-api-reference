# Send Bulk SMS with Sempico Solutions SMS

## Endpoint

- **Method:** `POST`
- **Path:** `/send-bulk`
- **Base URL:** `https://restapi.sempico.solutions/v1`
- **Official documentation:** [Send Bulk SMS](https://pypi.org/pypi/gatum-rest-py/json)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `senderID` | body | `string` | yes | Sender ID for the bulk message. |
| `text` | body | `string` | yes | Bulk SMS message text. |
| `id_group[]` | body | `array<number>` | yes | Group IDs to send the bulk SMS to. |
| `id_group_excluded[]` | body | `array<number>` | no | Optional group IDs to exclude from the sending. |
| `phone[]` | body | `array<string>` | no | Optional extra phone numbers to include. |
| `dateStart` | body | `date` | no | Optional date to start gradual sending. |
| `timeStart` | body | `string` | no | Optional start time for gradual sending. |
| `timeStop` | body | `string` | no | Optional stop time for gradual sending. |
