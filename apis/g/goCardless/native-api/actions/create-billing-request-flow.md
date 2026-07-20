# Create Billing Request Flow with GoCardless

Creates a new billing request flow in GoCardless.

## Endpoint

- **Method:** `POST`
- **Path:** `/billing_request_flows`
- **Base URL:** `https://api-sandbox.gocardless.com`
- **Official documentation:** [Create Billing Request Flow](https://developer.gocardless.com/api-reference/#billing-request-flows-create-a-billing-request-flow)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `redirect_uri` | body | `string` | no | URL to redirect the payer to after completing the request flow. |
| `exit_uri` | body | `string` | no | URL the payer can be taken to if the flow cannot progress. |
| `language` | body | `list<string>` | no | Default language of the billing request flow and the customer. Accepted values: `0`, `1`, `10`, `2`, `3`, `4`, `5`, `6`, `7`, `8`, `9`. |
| `skip_success_screen` | body | `boolean` | no | If true, the payer will not be redirected to the success screen after completing the flow. |
| `show_success_redirect_button` | body | `boolean` | no | If true, the payer will see a redirect action button on the Success page. |
| `prefilled_customer` | body | `object` | no | Prefilled customer details for the billing request flow. |
| `prefilled_customer.given_name` | body | `string` | no | Prefilled customer first name. |
| `prefilled_customer.family_name` | body | `string` | no | Prefilled customer surname. |
| `prefilled_customer.email` | body | `string` | no | Prefilled customer email address. |
| `links` | body | `object` | no | Related resource identifiers for this billing request flow. |
| `links.billing_request` | body | `string` | yes | ID of the billing request against which this flow was created. |
