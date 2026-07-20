# Start Domain Transfer In with GoDaddy CRM

Starts a domain transfer into GoDaddy.

## Endpoint

- **Method:** `POST`
- **Path:** `/v2/customers/:customerId/domains/:domain/transfer`
- **Base URL:** `https://api.godaddy.com`
- **Official documentation:** [Start Domain Transfer In](https://developer.godaddy.com/doc/endpoint/domains)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `customerId` | path | `string` | yes | The Customer identifier. Use the shopper ID unless you are operating on behalf of a reseller subaccount. |
| `domain` | path | `string` | yes | The domain name to transfer in. |
| `authCode` | body | `string` | yes | The authorization code for the transfer-in domain. |
| `consent` | body | `object` | yes | Consent details including agreedAt, agreedBy, and agreementKeys. |
| `period` | body | `number` | no | Transfer renewal period in years. |
| `renewAuto` | body | `boolean` | no | Whether the domain should automatically renew after transfer. |
| `privacy` | body | `boolean` | no | Whether privacy should be enabled. |
| `identityDocumentId` | body | `string` | no | Identity document identifier when required by the transfer schema. |
| `contacts` | body | `object` | no | Registrant and related contact objects when required by the transfer schema. |
| `metadata` | body | `object` | no | Additional metadata supported by the transfer schema. |
