# Create Template with SendPulse

Creates a new template in SendPulse.

## Endpoint

- **Method:** `POST`
- **Path:** `/template`
- **Base URL:** `https://api.sendpulse.com`
- **Official documentation:** [Create Template](https://sendpulse.com/integrations/api/bulk-email#create-template)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `name` | body | `string` | yes | Name of the template. |
| `body` | body | `string` | yes | Base64-encoded HTML body for the template. |
| `lang` | body | `string` | no | Optional template language code. |
