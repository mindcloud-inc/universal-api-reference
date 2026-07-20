# Delete Negotiated Rates with Ship&Co

## Endpoint

- **Method:** `DELETE`
- **Path:** `/carriers/:id/rates`
- **Base URL:** `https://api.shipandco.com/v1`
- **Official documentation:** [Delete Negotiated Rates](https://developer.shipandco.com/en/#negotiated-rates)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | Ship&Co carrier ID whose negotiated rates should be removed. Ship&Co requires a 17-character carrier ID. Maximum length: 17. |
