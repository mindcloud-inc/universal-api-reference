# Create New Contact with WhautoChat

Creates a new contact in WhautoChat.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/contacts`
- **Base URL:** `https://api.whauto.chat`
- **Official documentation:** [Create New Contact](https://help.whauto.chat/cloud-version/integrations/rest-api/endpoints/contacts/#2-create-new-contact)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `name` | body | `string` | no |
| `phoneNumber` | body | `string` | no |
| `workspace.id` | body | `string` | no |
| `stage` | body | `string` | no |
| `notes` | body | `string` | no |
| `customFields` | body | `object` | no |
| `tags[]` | body | `array<string>` | no |
