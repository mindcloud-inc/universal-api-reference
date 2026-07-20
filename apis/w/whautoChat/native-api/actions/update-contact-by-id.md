# Update Contact by ID with WhautoChat

Updates an existing contact in WhautoChat by ID.

## Endpoint

- **Method:** `PUT`
- **Path:** `/v1/contacts/{contactId}`
- **Base URL:** `https://api.whauto.chat`
- **Official documentation:** [Update Contact by ID](https://help.whauto.chat/cloud-version/integrations/rest-api/endpoints/contacts/#4-update-contact-by-id)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `contactId` | path | `string` | yes | Contact unique ID |
| `name` | body | `string` | no | — |
| `phoneNumber` | body | `string` | no | — |
| `workspace.id` | body | `string` | no | — |
| `stage` | body | `string` | no | — |
| `notes` | body | `string` | no | — |
| `customFields` | body | `object` | no | — |
| `tags[]` | body | `array<string>` | no | — |
