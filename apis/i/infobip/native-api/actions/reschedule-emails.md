# Reschedule Emails with Infobip

## Endpoint

- **Method:** `PUT`
- **Path:** `/email/1/bulks`
- **Base URL:** `https://rkpzwe.api.infobip.com`
- **Official documentation:** [Reschedule Emails](https://www.infobip.com/docs/api/channels/email)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `bulkId` | query | `string` | yes | The ID that uniquely identifies the sent bulk. |
| `sendAt` | body | `date` | yes | Date and time when the email is to be sent. Has the following format: `yyyy-MM-dd'T'HH:mm:ss.SSSZ`. |
