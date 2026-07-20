# Create Plan with BlueSnap

Creates a plan in BlueSnap.

## Endpoint

- **Method:** `POST`
- **Path:** `/recurring/plans`
- **Base URL:** `https://sandbox.bluesnap.com/services/2`
- **Official documentation:** [Create Plan](https://developers.bluesnap.com/v8976-JSON/reference/create-plan)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `name` | body | `string` | yes | Name of the billing plan. |
| `chargeFrequency` | body | `string` | yes | Charge frequency, e.g. MONTHLY. |
| `currency` | body | `string` | yes | Currency code (ISO 4217), e.g. USD. |
| `recurringChargeAmount` | body | `string` | yes | Recurring amount to charge. |
