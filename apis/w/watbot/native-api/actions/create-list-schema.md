# Create List Schema with Watbot

Creates a new list schema in Watbot.

## Endpoint

- **Method:** `POST`
- **Path:** `/createListSchema`
- **Base URL:** `https://watbot.ru/api/v1`
- **Official documentation:** [Create List Schema](https://docs.watbot.ru/rabota-s-api/spiski/spiski)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `name` | body | `string` | yes | Name of the list schema. |
| `fields` | body | `object` | yes | Field definitions for the list schema. |
| `is_menu` | body | `boolean` | no | Whether the list should appear in the Watbot menu. |
| `bot_id` | body | `number` | yes | ID of the Watbot bot that owns the list. |
