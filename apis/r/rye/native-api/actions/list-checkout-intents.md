# List Checkout Intents with Rye

Retrieves checkout intents from Rye.

## Endpoint

- **Method:** `GET`
- **Path:** `/api/v1/checkout-intents`
- **Base URL:** `https://staging.api.rye.com`
- **Official documentation:** [List Checkout Intents](https://rye.com/docs/api-v2/introduction)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id[]` | query | `array<string>` | no | Filter by checkout intent ids. Send multiple values as a array. |
| `state[]` | query | `array<string>` | no | Filter by checkout intent states. Send multiple values as a array. |
