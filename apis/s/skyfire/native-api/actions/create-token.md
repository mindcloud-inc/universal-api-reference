# Create Token with Skyfire

Creates a new token in Skyfire.

## Endpoint

- **Method:** `POST`
- **Path:** `/tokens`
- **Base URL:** `https://api.skyfire.xyz/api/v1`
- **Official documentation:** [Create Token](https://docs.skyfire.xyz/reference/create-token)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `type` | body | `string` | yes | One of kya, pay, or kya-pay. |
| `buyerTag` | body | `string` | no | Buyer internal identifier for the transaction or token. |
| `tokenAmount` | body | `string` | no | Amount for a pay or kya-pay token. |
| `sellerServiceId` | body | `string` | no | One of either sellerServiceId or sellerDomainOrUrl is required. |
| `sellerDomainOrUrl` | body | `string` | no | One of either sellerServiceId or sellerDomainOrUrl is required. |
| `expiresAt` | body | `number` | no | Seconds since the Unix epoch. |
| `identityPermissions[]` | body | `array<string>` | no | Additional identity fields to include in the token. |
