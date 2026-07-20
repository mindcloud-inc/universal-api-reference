# List Event Attendees with Billetweb

Retrieves attendees for a Billetweb event.

## Endpoint

- **Method:** `GET`
- **Path:** `/event/:id/attendees`
- **Base URL:** `https://www.billetweb.fr/api`
- **Official documentation:** [List Event Attendees](https://www.billetweb.fr/bo/api.php#/api/event/:id/attendees)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `number` | yes | Event identifier. |
| `last_update` | query | `number` | no | Only return attendees updated after this Unix timestamp. |
| `since` | query | `number` | no | Only return attendees updated during the last N minutes. |
| `to` | query | `number` | no | Only return attendees modified before this Unix timestamp. |
| `session` | query | `string` | no | Filter by a specific session identifier. |
| `futur_sessions` | query | `boolean` | no | Only include non-past sessions. |
| `used` | query | `number` | no | Filter by check-in state. |
| `ticket` | query | `number` | no | Filter by ticket identifier. |
| `email` | query | `string` | no | Filter by buyer email. |
| `ext_id` | query | `string` | no | Filter by external ticket identifier. |
| `barcode` | query | `string` | no | Filter by barcode. |
| `disabled` | query | `number` | no | Include refunded or canceled tickets. |
