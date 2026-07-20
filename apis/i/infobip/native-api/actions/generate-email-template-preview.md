# Generate Email Template Preview with Infobip

## Endpoint

- **Method:** `POST`
- **Path:** `/email/1/templates/{templateId}/preview`
- **Base URL:** `https://rkpzwe.api.infobip.com`
- **Official documentation:** [Generate Email Template Preview](https://www.infobip.com/docs/api/channels/email)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `templateId` | path | `number` | yes | Unique identifier (ID) of the email template. |
| `placeholders` | body | `object` | no | A map of placeholder names and their replacement values. |
