# Deactivate Agent Seller Service with Skyfire

Deactivates an existing agent seller service in Skyfire.

## Endpoint

- **Method:** `POST`
- **Path:** `/agents/seller-services/:sellerServiceId/deactivate`
- **Base URL:** `https://api.skyfire.xyz/api/v1`
- **Official documentation:** [Deactivate Agent Seller Service](https://docs.skyfire.xyz/reference/deactivate-agents-service)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `sellerServiceId` | path | `string` | yes | The ID of the seller service to deactivate. |
