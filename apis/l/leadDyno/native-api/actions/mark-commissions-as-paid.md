# Mark Commissions As Paid with LeadDyno

Marks affiliate commissions as paid for a purchase in LeadDyno.

## Endpoint

- **Method:** `POST`
- **Path:** `/commissions/mark_as_paid`
- **Base URL:** `https://api.leaddyno.com/v1`
- **Official documentation:** [Mark Commissions As Paid](https://app.theneo.io/leaddyno/leaddyno-rest-api/commissions/mark-affiliate-commissions-as-paid)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `affiliate_email` | body | `string` | yes | The affiliate e-mail the payment is directed to. |
| `purchase_code` | body | `string` | yes | The purchase that originated the commissions. |
