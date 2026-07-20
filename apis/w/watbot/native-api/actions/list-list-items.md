# List List Items with Watbot

Retrieves list items from a Watbot list schema.

## Endpoint

- **Method:** `POST`
- **Path:** `/getListItems`
- **Base URL:** `https://watbot.ru/api/v1`
- **Official documentation:** [List List Items](https://docs.watbot.ru/rabota-s-api/spiski/elementy-spiska)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `schema_id` | body | `string` | yes | ID of the list schema. |
| `bot_id` | body | `number` | no | Bot ID if the schema has a bot field. |
| `contact_id` | body | `number` | no | Contact ID if the schema has a contact field. |
| `order_by` | body | `string` | no | Sort field or field,direction expression. |
| `filters` | body | `object` | no | Filter object for list item fields. |
| `page` | body | `object` | no | Page selection payload. |
| `limit` | body | `number` | no | Maximum number of items to return. |
