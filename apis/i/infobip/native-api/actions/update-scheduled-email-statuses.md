# Update Scheduled Email Statuses with Infobip

## Endpoint

- **Method:** `PUT`
- **Path:** `/email/1/bulks/status`
- **Base URL:** `https://rkpzwe.api.infobip.com`
- **Official documentation:** [Update Scheduled Email Statuses](https://www.infobip.com/docs/api/channels/email)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `bulkId` | query | `string` | yes | The ID that uniquely identifies the sent bulk. |
| `status` | body | `string` | yes | Status of scheduled email messages. |
