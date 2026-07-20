# List Consignment with Megaplan

## Endpoint

- **Method:** `GET`
- **Path:** `/consignment`
- **Base URL:** `https://m60888876.megaplan.ru/api/v3`
- **Official documentation:** [List Consignment](https://m60888876.megaplan.ru/api/v3/docs#consignment)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `q` | query | `string` | no | NO_DESCRIPTION |
| `filter` | query | `string` | no | NO_DESCRIPTION |
| `pageAfter` | query | `object` | no | Загрузить страницу, начиная с переданной сущности. |
| `pageBefore` | query | `object` | no | Загрузить страницу строго до переданной сущности. |
| `pageWith` | query | `object` | no | Загрузить страницу c наличием переданной сущности. |
| `limit` | query | `number` | no | Сколько элементов включать в страницу. |
| `fields` | query | `object` | no | Набор дополнительных полей, включённых в список |
| `sortBy[]` | query | `array` | no | массив полей сортировки |
| `onlyRequestedFields` | query | `boolean` | no | отдавать только перечисленные поля |
