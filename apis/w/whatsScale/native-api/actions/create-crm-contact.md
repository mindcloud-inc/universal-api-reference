# Create CRM Contact with WhatsScale

Creates a CRM contact in WhatsScale.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/crm/contacts`
- **Base URL:** `https://proxy.whatsscale.com`
- **Official documentation:** [Create CRM Contact](https://whatsscale.com/docs)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `name` | body | `string` | no | Optional contact display name. |
| `phone` | body | `string` | yes | Contact phone number. |
| `tags[]` | body | `array<string>` | no | Optional contact tags. Send multiple values as a array. |
