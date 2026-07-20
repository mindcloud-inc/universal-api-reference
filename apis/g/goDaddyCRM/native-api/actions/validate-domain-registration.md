# Validate Domain Registration with GoDaddy CRM

Validates a domain registration in GoDaddy.

## Endpoint

- **Method:** `POST`
- **Path:** `/v2/customers/:customerId/domains/register/validate`
- **Base URL:** `https://api.godaddy.com`
- **Official documentation:** [Validate Domain Registration](https://developer.godaddy.com/doc/endpoint/domains)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `customerId` | path | `string` | yes | The Customer identifier. Use the shopper ID unless you are operating on behalf of a reseller subaccount. |
| `domain` | body | `string` | yes | The domain name to validate for registration. |
| `consent` | body | `object` | yes | Consent details including agreedAt, agreedBy, and agreementKeys. |
| `period` | body | `number` | no | Registration period in years. |
| `nameServers[]` | body | `array<string>` | no | Custom name servers for the domain. |
| `renewAuto` | body | `boolean` | no | Whether the domain should automatically renew. |
| `privacy` | body | `boolean` | no | Whether privacy should be enabled. |
| `contacts` | body | `object` | no | Registrant and related contact objects when required by the TLD schema. |
| `metadata` | body | `object` | no | Additional metadata supported by the registration schema. |
