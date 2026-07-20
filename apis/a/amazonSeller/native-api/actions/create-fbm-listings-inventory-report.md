# Create FBM Listings Inventory Report with Amazon Seller

Creates an FBM listings inventory report in Amazon Seller.

## Endpoint

- **Method:** `POST`
- **Path:** `reports/2021-06-30/reports`
- **Base URL:** `https://{environment}-{region}.amazon.com`
- **API:** REST
- **Official documentation:** [Create FBM Listings Inventory Report](https://developer-docs.amazon.com/sp-api/docs/reports-api-v2021-06-30-reference#createreport)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `reportType` | body | `list` | yes | Accepted values: `GET_MERCHANT_LISTINGS_DATA`, `GET_MERCHANT_LISTINGS_DATA_LITER`. |
| `marketplaceIds` | body | `object<string>` | yes | — |
| `dataStartTime` | body | `date` | no | — |
| `dataEndTime` | body | `date` | no | — |
| `reportOptions` | body | `object` | no | — |
