# Update Agent Seller Service with Skyfire

Updates an existing agent seller service in Skyfire.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/agents/seller-services/:sellerServiceId`
- **Base URL:** `https://api.skyfire.xyz/api/v1`
- **Official documentation:** [Update Agent Seller Service](https://docs.skyfire.xyz/reference/update-agents-service)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `description` | body | `string` | no | New description of the service. |
| `name` | body | `string` | no | New name of the service. |
| `sellerServiceId` | path | `string` | yes | The ID of the seller service to update. |
| `tags[]` | body | `array<string>` | no | New tags for the service. |
| `minimumTokenAmount` | body | `string` | no | New minimum amount in USD that buyers must set on their tokens. |
| `price` | body | `string` | no | New price of the service in USD. |
| `acceptedTokens[]` | body | `array<string>` | no | List of token types the seller service accepts. Must be one or more of kya, pay, and kya-pay. |
