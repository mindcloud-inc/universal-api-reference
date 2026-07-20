# List Product Categories with Botbaba

## Endpoint

- **Method:** `GET`
- **Path:** `/api/GetProductCategories`
- **Base URL:** `https://app.botbaba.io`
- **Official documentation:** [List Product Categories](https://app.botbaba.io/swagger/ui/index)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `botId` | query | `number` | yes | The Botbaba bot identifier. |
| `searchKey` | query | `string` | no | Optional search text for category names. |
