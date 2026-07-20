# Update Deal Field with BoardCRM

Updates an existing deal field in BoardCRM.

## Endpoint

- **Method:** `POST`
- **Path:** `/field/update`
- **Base URL:** `https://api.boardcrm.io/api`
- **Official documentation:** [Update Deal Field](https://dev.boardcrm.io/public/0.1/methods/field#update)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | body | `number` | yes | Field ID. |
| `title` | body | `string` | no | Updated field title. |
| `sorting` | body | `number` | no | Updated field sort order. |
