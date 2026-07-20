# Search Tourists with U-ON

Finds tourists in U-ON by search criteria.

## Endpoint

- **Method:** `POST`
- **Path:** `/user/search.json`
- **Base URL:** `https://api.u-on.ru/{key}`
- **Official documentation:** [Search Tourists](https://api.u-on.travel/doc)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `passport` | body | `string` | no | Серия и номер гражданского паспорта / Passport number |
| `zagran_passport` | body | `string` | no | Серия и номер заграничного паспорта / Foreign passport number |
| `vkontakte` | body | `string` | no | Аккаунт в Vkontakte / Vkontakte account |
| `facebook` | body | `string` | no | Аккаунт в Facebook / Facebook account |
| `odnoklassniki` | body | `string` | no | Аккаунт в Odnoklassniki / Odnoklassniki account |
| `telegram` | body | `string` | no | Аккаунт в Telegram / Telegram account |
| `max` | body | `string` | no | Аккаунт в MAX / MAX account |
| `whatsapp` | body | `string` | no | Аккаунт в Whatsapp / Whatsapp account |
| `viber` | body | `string` | no | Аккаунт в Viber / Viber account |
| `instagram` | body | `string` | no | Аккаунт в Instagram / Instagram account |
| `label_ids` | body | `string` | no | ID меток через запятую / Labels ID (delimited by comma) |
| `part_match` | body | `number` | no | Полное совпадение (по-умолчанию) или частичное (=1) / Full match (by default) or part match (=1) |
| `page` | body | `number` | no | Номер страницы выдачи (по-умолчанию, 1) / Page number (by default, 1) |
