# List Customer Redemptions with Vouchery.io

## Endpoint

- **Method:** `GET`
- **Path:** `/customers/:identifier/redemptions`
- **Base URL:** `https://mindcloud.sandbox.vouchery.app/api/v2.1`
- **Official documentation:** [List Customer Redemptions](https://docs.vouchery.io/reference/getapiv21customersidentifierredemptions)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `identifier` | path | `string` | yes | Customer Identifier |
| `page` | query | `number` | no | Result page (indexed from 1) |
| `per_page` | query | `number` | no | Results per page |
