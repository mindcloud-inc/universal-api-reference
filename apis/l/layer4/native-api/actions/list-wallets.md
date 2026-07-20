# List Wallets with Layer4

Retrieves wallets from Layer4.

## Endpoint

- **Method:** `GET`
- **Path:** `/api/v1/wallets`
- **Base URL:** `https://www.layer4.app`
- **Official documentation:** [List Wallets](https://www.layer4.app/api-docs#tag/Wallets/operation/WalletsController_findAll)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `status[]` | query | `array<string>` | no | Filter wallets by one or more statuses: ACTIVE, PENDING, or DECLINED. |
