# Purchase Domains with SuperSend

Creates managed domains in SuperSend.

## Endpoint

- **Method:** `POST`
- **Path:** `/domains/purchase`
- **Base URL:** `https://api.supersend.io/v2`
- **Official documentation:** [Purchase Domains](https://docs.supersend.io/docs/managed-domain)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `domains[]` | body | `array<string>` | yes |
| `paymentMethodId` | body | `string` | yes |
| `forwardingAddress` | body | `string` | yes |
| `contactDetails` | body | `object` | yes |
| `dmarcEmail` | body | `string` | no |
