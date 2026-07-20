# Purchase Domains and Mailboxes with SuperSend

Creates managed domains and mailboxes in SuperSend.

## Endpoint

- **Method:** `POST`
- **Path:** `/domains/purchase-with-mailboxes`
- **Base URL:** `https://api.supersend.io/v2`
- **Official documentation:** [Purchase Domains and Mailboxes](https://docs.supersend.io/docs/managed-domain)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `domains[]` | body | `array<string>` | no | — |
| `domainsWithProviders[]` | body | `array<object>` | no | — |
| `domainsWithProviders[].domain` | body | `string` | no | — |
| `domainsWithProviders[].provider` | body | `string` | no | Allowed values: google, outlook, smtp. |
| `mailboxes[]` | body | `array<object>` | no | — |
| `mailboxes[].username` | body | `string` | no | — |
| `mailboxes[].firstName` | body | `string` | no | — |
| `mailboxes[].lastName` | body | `string` | no | — |
| `mailboxes[].domain` | body | `string` | no | — |
| `mailboxes[].signature` | body | `string` | no | — |
| `mailboxes[].provider` | body | `string` | no | Allowed values: google, outlook, smtp. |
| `paymentMethodId` | body | `string` | yes | — |
| `TeamId` | body | `string` | no | — |
| `forwardingAddress` | body | `string` | no | — |
| `dmarcEmail` | body | `string` | no | — |
| `contactDetails` | body | `object` | no | — |
| `saveContactAsDefault` | body | `boolean` | no | — |
