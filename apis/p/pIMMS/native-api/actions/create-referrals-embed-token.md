# Create Referrals Embed Token with PIMMS

Creates a new referrals embed token in PIMMS.

## Endpoint

- **Method:** `POST`
- **Path:** `/tokens/embed/referrals`
- **Base URL:** `https://api.pimms.io`
- **Official documentation:** [Create Referrals Embed Token](https://pimms.apidocumentation.com/reference#tag/embed-tokens/POST/tokens/embed/referrals)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `programId` | body | `string` | yes | Referral program ID used to create the embed token. |
| `partnerId` | body | `string` | no | — |
| `tenantId` | body | `string` | no | — |
| `partner` | body | `object` | no | — |
