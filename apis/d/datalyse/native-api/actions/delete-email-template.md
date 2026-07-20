# Delete Email Template with Datalyse

Deletes an existing email template from Datalyse.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/1.0/emails/templates/delete.json`
- **Base URL:** `https://api.datalyse.io`
- **Official documentation:** [Delete Email Template](https://developers.datalyse.io/devs/content_api.html)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `template_id` | body | `string` | yes | ID of the template to delete |
