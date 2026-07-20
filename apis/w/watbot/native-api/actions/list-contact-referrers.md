# List Contact Referrers with Watbot

Retrieves referrers for a Watbot contact.

## Endpoint

- **Method:** `GET`
- **Path:** `/getReferrers`
- **Base URL:** `https://watbot.ru/api/v1`
- **Official documentation:** [List Contact Referrers](https://docs.watbot.ru/rabota-s-api/kontakty/referalnaya-sistema)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `contact_id` | query | `number` | yes | ID контакта. |
| `depth` | query | `number` | no | Глубина дерева от 1 до 10. |
| `is_flat` | query | `boolean` | no | 1 — вернуть плоский список вместо дерева. |
