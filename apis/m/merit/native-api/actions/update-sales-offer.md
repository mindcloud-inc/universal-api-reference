# Update Sales Offer with Merit

## Endpoint

- **Method:** `POST`
- **Path:** `v2/updateoffer`
- **Base URL:** `https://aktiva.merit.ee/api`
- **Official documentation:** [Update Sales Offer](https://api.merit.ee/connecting-robots/reference-manual/sales-offers/update-sales-offer/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `OfferNo` | body | `string` | yes | Sales offer number from Merit docs. |
| `HComment` | body | `string` | no | Header comment update from Merit docs. |
