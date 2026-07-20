# Count Referral Network with Watbot

Retrieves referral network counts for a Watbot contact.

## Endpoint

- **Method:** `POST`
- **Path:** `/getCountReferrals`
- **Base URL:** `https://watbot.ru/api/v1`
- **Official documentation:** [Count Referral Network](https://docs.watbot.ru/rabota-s-api/kontakty/referalnaya-sistema)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `contact_id` | query | `number` | yes | ID контакта. |
| `filters` | query | `object` | no | Объект фильтров. Поддерживаются tag_name и tag_id, включая массивы значений. |
