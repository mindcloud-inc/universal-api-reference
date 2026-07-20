# Update Template with SendPulse

Updates an existing template in SendPulse.

## Endpoint

- **Method:** `POST`
- **Path:** `/template/edit/:templateId`
- **Base URL:** `https://api.sendpulse.com`
- **Official documentation:** [Update Template](https://sendpulse.com/integrations/api/bulk-email#edit-template)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `templateId` | path | `string` | yes | The SendPulse template identifier. |
| `name` | body | `string` | no | Updated name for the template. |
| `body` | body | `string` | yes | Updated base64-encoded HTML body for the template. |
| `lang` | body | `string` | no | Optional template language code. |
