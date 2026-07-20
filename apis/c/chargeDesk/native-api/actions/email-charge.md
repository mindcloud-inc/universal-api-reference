# Email Charge with ChargeDesk

Emails a charge from ChargeDesk.

## Endpoint

- **Method:** `POST`
- **Path:** `/charges/:CHARGE_ID/email`
- **Base URL:** `https://api.chargedesk.com/v1`
- **Official documentation:** [Email Charge](https://chargedesk.com/api-docs#charges-email-charge)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `CHARGE_ID` | path | `string` | yes | Charge ID whose receipt email should be sent. |
| `email` | body | `string` | no | Email address to send the charge notification to. |
