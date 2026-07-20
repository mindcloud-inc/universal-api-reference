# Update Contact Status with JustCall

Updates contact status in JustCall.

## Endpoint

- **Method:** `PUT`
- **Path:** `/v2.1/contacts/status`
- **Base URL:** `https://api.justcall.io`
- **Official documentation:** [Update Contact Status](https://developer.justcall.io/reference/update_contact_status_v21)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `add_to[]` | body | `array<string>` | no | Status lists to add the contact to. |
| `id` | body | `number` | no | The JustCall contact ID whose status should change. |
