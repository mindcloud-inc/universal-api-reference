# List Events with SuperSend

Retrieves events from SuperSend.

## Endpoint

- **Method:** `GET`
- **Path:** `/events`
- **Base URL:** `https://api.supersend.io/v2`
- **Official documentation:** [List Events](https://docs.supersend.io/docs/event)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `TeamId` | query | `string` | no | — |
| `CampaignId` | query | `string` | no | — |
| `ContactId` | query | `string` | no | — |
| `SenderId` | query | `string` | no | — |
| `type` | query | `string` | no | Allowed values: scheduled, sent, open, reply, click, bounce, unsubscribe. |
| `channel` | query | `string` | no | Allowed values: email, linkedin, twitter, text, call. |
| `limit` | query | `number` | no | Default: 50. Range: 1 to 100. |
| `offset` | query | `number` | no | Default: 0. Range: 0 to inf. |
| `start_date` | query | `date` | no | Filter events after this date (ISO 8601) |
| `end_date` | query | `date` | no | Filter events before this date (ISO 8601) |
