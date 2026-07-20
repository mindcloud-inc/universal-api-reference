# Get Extra Fees Pricing with LimoExpress

Retrieves extra fee pricing in LimoExpress by currency and vehicle class.

## Endpoint

- **Method:** `GET`
- **Path:** `/api/integration/extra-fees-pricing/:currencyId/:vehicleClassId`
- **Base URL:** `https://api.limoexpress.me`
- **Official documentation:** [Get Extra Fees Pricing](https://api.limoexpress.me/api/docs/v1#/Website%20Integration/getExtraFeesPricing)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `currencyId` | path | `string` | yes | Currency identifier path parameter. |
| `vehicleClassId` | path | `string` | yes | Vehicle class identifier path parameter. |
