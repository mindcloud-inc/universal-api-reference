# Delete Carrier with Ship&Co

## Endpoint

- **Method:** `DELETE`
- **Path:** `/carriers/:id`
- **Base URL:** `https://api.shipandco.com/v1`
- **Official documentation:** [Delete Carrier](https://developer.shipandco.com/en/#carrier)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | Ship&Co carrier ID to delete. Ship&Co requires a 17-character carrier ID. Maximum length: 17. |
