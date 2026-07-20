# Establish Two-Legged Call with Aloware

Establishes a two-legged call in Aloware.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/v1/webhook/two-legged-call`
- **Base URL:** `https://app.aloware.com`
- **Official documentation:** [Establish Two-Legged Call](https://support.aloware.com/en/articles/9019991-api-documentation-aloware-two-legged-call-api-integration)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `user_id` | body | `string` | no | User ID for the agent leg. Provide this or Ring Group ID. |
| `ring_group_id` | body | `string` | no | Ring group ID for the agent leg. Provide this or User ID. |
| `contact_phone_number` | body | `string` | no | Contact phone number. Provide this or Contact ID. |
| `contact_id` | body | `string` | no | Contact ID. Provide this or Contact Phone Number. |
| `line_phone_number` | body | `string` | no | Aloware line phone number. Provide this or Line ID. |
| `line_id` | body | `string` | no | Aloware line ID. Provide this or Line Phone Number. |
| `user_phone_number` | body | `string` | no | Optional user phone number when starting a call with User ID. |
