# Get Receipt with EenvoudigFactureren

Retrieves a receipt from EenvoudigFactureren.

## Endpoint

- **Method:** `GET`
- **Path:** `/receipts/:receipt_id`
- **Base URL:** `https://eenvoudigfactureren.be/api/v1`
- **Official documentation:** [Get Receipt](https://help.eenvoudigfactureren.be/support/solutions/articles/101000381980-api-kasticketten)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `receipt_id` | path | `string` | yes | EenvoudigFactureren receipt ID. |
