# List Products with Botbaba

## Endpoint

- **Method:** `GET`
- **Path:** `/api/GetProducts`
- **Base URL:** `https://app.botbaba.io`
- **Official documentation:** [List Products](https://app.botbaba.io/swagger/ui/index)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `botId` | query | `number` | yes | The Botbaba bot identifier. |
| `page` | query | `number` | no | Optional result page number. |
| `pageSize` | query | `number` | no | Optional page size. |
| `searchKey` | query | `string` | no | Optional search text for products. |
