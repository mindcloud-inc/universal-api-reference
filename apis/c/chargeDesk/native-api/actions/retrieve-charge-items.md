# Retrieve Charge Items with ChargeDesk

Retrieves charge items from ChargeDesk.

## Endpoint

- **Method:** `GET`
- **Path:** `/charges/:CHARGE_ID/items`
- **Base URL:** `https://api.chargedesk.com/v1`
- **Official documentation:** [Retrieve Charge Items](https://chargedesk.com/api-docs#charges-retrieve-items)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `CHARGE_ID` | path | `string` | yes | Charge ID whose line items should be retrieved. |
