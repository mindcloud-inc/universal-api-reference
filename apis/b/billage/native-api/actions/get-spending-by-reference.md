# Get Spending by Reference with Billage

Retrieves a spending from Billage by reference code.

## Endpoint

- **Method:** `GET`
- **Path:** `/v2/spendings/by-ref`
- **Base URL:** `https://app.getbillage.com/api`
- **Official documentation:** [Get Spending by Reference](https://app.getbillage.com/api/documentation.html#/Spendings/spendingByRef)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `serie` | query | `string` | no | Spending serie |
| `ref` | query | `string` | yes | Spending reference |
