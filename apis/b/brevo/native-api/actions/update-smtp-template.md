# Update SMTP Template with Brevo

## Endpoint

- **Method:** `PUT`
- **Path:** `/v3/smtp/templates/:templateId`
- **Base URL:** `https://api.brevo.com`
- **Official documentation:** [Update SMTP Template](https://developers.brevo.com/reference/update-smtp-template)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `subject` | body | `string` | no | Updated default subject line. |
| `templateId` | path | `string` | yes | SMTP template ID. |
