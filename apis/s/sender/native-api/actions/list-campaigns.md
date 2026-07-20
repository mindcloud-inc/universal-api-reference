# List Campaigns with Sender

## Endpoint

- **Method:** `GET`
- **Path:** `/campaigns`
- **Base URL:** `https://api.sender.net/v2`
- **Official documentation:** [List Campaigns](https://api.sender.net/campaigns/get-all/)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `status[]` | query | `array<string>` | no | Filter campaigns by status: SCHEDULED, SENDING, SENT, or DRAFT. |
