# Collect Billing Request Customer Details with GoCardless

Collects customer details for a GoCardless billing request.

## Endpoint

- **Method:** `POST`
- **Path:** `/billing_requests/:billingRequestId/actions/collect_customer_details`
- **Base URL:** `https://api-sandbox.gocardless.com`
- **Official documentation:** [Collect Billing Request Customer Details](https://developer.gocardless.com/api-reference/#billing-requests-collect-customer-details)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `billingRequestId` | path | `string` | yes | ID of the billing request whose customer details should be collected. |
| `customer` | body | `object` | no | Customer fields to collect for the billing request. |
| `customer.email` | body | `string` | no | Customer email address. |
| `customer.given_name` | body | `string` | no | Customer first name. |
| `customer.family_name` | body | `string` | no | Customer surname. |
| `customer.company_name` | body | `string` | no | Customer company name. |
| `customer.language` | body | `list<string>` | no | ISO 639-1 language code for customer notifications. Accepted values: `0`, `1`, `10`, `2`, `3`, `4`, `5`, `6`, `7`, `8`, `9`. |
| `customer.phone_number` | body | `string` | no | Customer phone number in ITU E.123 format. |
| `customer.metadata` | body | `object` | no | Key-value store of custom data for the customer. |
| `customer_billing_detail` | body | `object` | no | Customer billing detail fields to collect for the billing request. |
| `customer_billing_detail.address_line1` | body | `string` | no | First line of the customer's address. |
| `customer_billing_detail.city` | body | `string` | no | City of the customer's address. |
| `customer_billing_detail.postal_code` | body | `string` | no | Postal code for the customer's address. |
| `customer_billing_detail.country_code` | body | `string` | no | ISO 3166-1 alpha-2 country code. |
| `customer_billing_detail.region` | body | `string` | no | Region, county, or department for the address. |
| `customer_billing_detail.ip_address` | body | `string` | no | Payer IP address for ACH customers. |
