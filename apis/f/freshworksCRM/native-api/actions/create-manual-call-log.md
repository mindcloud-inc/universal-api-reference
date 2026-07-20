# Create Manual Call Log with Freshworks CRM

Creates a manual call log in Freshworks CRM.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/phone_calls`
- **Base URL:** `https://{bundleAlias}`
- **Official documentation:** [Create Manual Call Log](https://developers.freshworks.com/crm/api/#manual_call_log)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `phone_call` | body | `object` | yes | Manual call log payload |
| `phone_call.call_direction` | body | `boolean` | yes | Directional flag for the manual call log |
| `phone_call.note` | body | `object` | no | Optional note payload |
| `phone_call.targetable` | body | `object` | yes | Linked contact/account payload |
| `phone_call.targetable_type` | body | `string` | yes | Entity type for the linked record |
