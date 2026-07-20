# Renew Domain with GoDaddy CRM

Renews a domain in your GoDaddy account.

## Endpoint

- **Method:** `POST`
- **Path:** `/v2/customers/:customerId/domains/:domain/renew`
- **Base URL:** `https://api.godaddy.com`
- **Official documentation:** [Renew Domain](https://developer.godaddy.com/doc/endpoint/domains)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `customerId` | path | `string` | yes | The Customer identifier. Use the shopper ID unless you are operating on behalf of a reseller subaccount. |
| `domain` | path | `string` | yes | The domain name to renew. |
| `expires` | body | `date` | yes | The resulting expiration timestamp for the renewed domain. |
| `consent` | body | `object` | yes | Consent details including agreedAt, agreedBy, and agreementKeys. |
| `period` | body | `number` | no | Renewal period in years. |
