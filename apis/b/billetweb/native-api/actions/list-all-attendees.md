# List All Attendees with Billetweb

Retrieves attendees across all Billetweb events.

## Endpoint

- **Method:** `GET`
- **Path:** `/attendees`
- **Base URL:** `https://www.billetweb.fr/api`
- **Official documentation:** [List All Attendees](https://www.billetweb.fr/bo/api.php#/api/attendees)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `last_update` | query | `number` | no | Only return attendees updated after this Unix timestamp. |
| `since` | query | `number` | no | Only return attendees updated during the last N minutes. |
| `to` | query | `number` | no | Only return attendees modified before this Unix timestamp. |
| `tag` | query | `string` | no | Filter attendees for events containing a specific tag. |
| `futur` | query | `boolean` | no | Only include unfinished events. |
| `email` | query | `string` | no | Filter by buyer email. |
| `ticket` | query | `number` | no | Filter by ticket identifier. |
| `session` | query | `string` | no | Filter by session identifier. |
| `used` | query | `number` | no | Filter by check-in state. |
| `disabled` | query | `number` | no | Include refunded or canceled tickets. |
