# List Contact Referrals with Watbot

Retrieves referrals for a Watbot contact.

## Endpoint

- **Method:** `POST`
- **Path:** `/getReferrals`
- **Base URL:** `https://watbot.ru/api/v1`
- **Official documentation:** [List Contact Referrals](https://docs.watbot.ru/rabota-s-api/kontakty/referalnaya-sistema)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `contact_id` | query | `number` | yes | ID контакта. |
| `page` | query | `number` | no | Номер страницы результатов. |
| `filters` | query | `object` | no | Объект фильтров. Поддерживаются tag_name и tag_id, включая массивы значений. |
