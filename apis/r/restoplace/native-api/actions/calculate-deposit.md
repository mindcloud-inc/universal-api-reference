# Calculate Deposit with Restoplace

Calculates a deposit in Restoplace.

## Endpoint

- **Method:** `POST`
- **Path:** `/deposit/`
- **Base URL:** `https://api.restoplace.cc`
- **Official documentation:** [Calculate Deposit](https://restoplace.cc/help/API)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `from` | body | `string` | no | Reservation start date and time for the deposit calculation. |
| `to` | body | `string` | no | Reservation end date and time for the deposit calculation. |
| `count` | body | `number` | no | Number of guests for the deposit calculation. |
| `item_ids[]` | body | `array<number>` | no | Booking item IDs included in the deposit calculation. |
| `waitlist` | body | `number` | no | Whether the requested slot should be treated as a waitlist request. |
