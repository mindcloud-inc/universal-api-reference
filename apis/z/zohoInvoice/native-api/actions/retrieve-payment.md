# Retrieve Payment with Zoho Invoice

Retrieves a payment from Zoho Invoice.

## Endpoint

- **Method:** `GET`
- **Path:** `/customerpayments/:payment_id`
- **Base URL:** `https://www.zohoapis.com/invoice/v3`
- **Official documentation:** [Retrieve Payment](https://www.zoho.com/invoice/api/v3/customer-payments/#retrieve-a-payment)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `organization_id` | query | `list<string>` | yes | ID of the organization header X-com-zoho-invoice-organizationid. |
| `payment_id` | path | `string` | yes | Unique identifier of the payment. |
