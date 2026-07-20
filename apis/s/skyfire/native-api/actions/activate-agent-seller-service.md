# Activate Agent Seller Service with Skyfire

Activates an existing agent seller service in Skyfire.

## Endpoint

- **Method:** `POST`
- **Path:** `/agents/seller-services/:sellerServiceId/activate`
- **Base URL:** `https://api.skyfire.xyz/api/v1`
- **Official documentation:** [Activate Agent Seller Service](https://docs.skyfire.xyz/reference/create-agents-service)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `sellerServiceId` | path | `string` | yes | The ID of the seller service to activate. |
