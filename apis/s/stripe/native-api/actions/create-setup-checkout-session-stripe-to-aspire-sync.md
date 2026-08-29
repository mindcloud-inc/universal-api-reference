# Create Setup Checkout Session – Stripe to Aspire Sync with Stripe

## Endpoint

- **Method:** `POST`
- **Path:** `checkout/sessions`
- **Base URL:** `https://api.stripe.com/v1`
- **Official documentation:** [Create Setup Checkout Session – Stripe to Aspire Sync](https://docs.stripe.com/api/checkout/sessions/create)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `customer` | body | `string` | no | Stripe Customer ID, supplied dynamically. |
| `customer_email` | body | `string` | no | Customer email when no Stripe Customer ID is supplied. |
| `success_url` | body | `string` | yes | Hosted Checkout success redirect URL. |
| `cancel_url` | body | `string` | yes | Hosted Checkout cancellation redirect URL. |
| `payment_method_types[]` | body | `array<string>` | yes | Allowed Stripe payment method types. Each value must be card or us_bank_account. Send multiple values as a array. |
| `client_reference_id` | body | `string` | yes | Unique MindCloud request ID used to reconcile the Checkout Session. |
| `meta_contract_version` | body | `string` | yes | Exact Stripe to Aspire metadata contract version. |
| `meta_mindcloud_request_id` | body | `string` | yes | Unique request identifier matching the payment reference contract. |
| `meta_payment_kind` | body | `string` | yes | Payment kind: deposit or invoice. |
| `meta_aspire_opportunity_number` | body | `string` | yes | Aspire Opportunity number audit link. |
| `meta_aspire_opportunity_revision` | body | `string` | yes | Aspire Opportunity revision. |
| `meta_aspire_billing_company` | body | `string` | yes | Aspire billing company; use the exact non-empty sentinel "none" only when the billing contact is populated. |
| `meta_aspire_billing_contact` | body | `string` | yes | Aspire billing contact; use the exact non-empty sentinel "none" only when the billing company is populated. |
| `meta_aspire_property` | body | `string` | yes | Aspire property audit context. |
| `meta_aspire_branch_name` | body | `string` | yes | Aspire branch name. |
| `meta_aspire_invoice_number` | body | `string` | yes | Use the exact non-empty sentinel "none" for deposits; use a positive integer string for invoice payments. |
| `meta_deposit_percent` | body | `string` | yes | Deposit percentage string for deposits; use the exact non-empty sentinel "none" for invoice payments. |
| `meta_deposit_basis_cents` | body | `string` | yes | Positive canonical integer-cent basis for deposits; use the exact non-empty sentinel "none" for invoice payments. |
| `meta_service_amount_cents` | body | `string` | yes | Canonical non-negative integer service amount in cents. |
| `meta_service_tax_cents` | body | `string` | yes | Canonical non-negative integer service sales tax in cents. |
| `meta_card_fee_cents` | body | `string` | yes | Canonical non-negative integer customer card fee in cents. |
| `meta_card_fee_tax_cents` | body | `string` | yes | Canonical non-negative integer sales tax on the card fee in cents. |
| `meta_currency` | body | `string` | yes | Exact lowercase metadata currency code. |
