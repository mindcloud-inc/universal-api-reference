# Get Ad Spend with Octanist

Retrieves ad spend data from Octanist.

## Endpoint

- **Method:** `POST`
- **Path:** `/ad-spend`
- **Base URL:** `https://octanist.com/api`
- **Official documentation:** [Get Ad Spend](https://octanist.com/docs/api-reference/endpoint/ad-spend)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `startDate` | body | `string` | yes | Start date in YYYY-MM-DD format. |
| `endDate` | body | `string` | yes | End date in YYYY-MM-DD format. |
| `platform` | body | `string` | no | Filter ad spend by platform. |
| `groupBy` | body | `string` | no | Dimension to group ad spend by. |
| `limit` | body | `number` | no | Results per page. |
| `page` | body | `number` | no | Page number. |
