# List Campaigns with Sarbacane

Retrieves campaigns from your Sarbacane account.

## Endpoint

- **Method:** `GET`
- **Path:** `/campaigns`
- **Base URL:** `https://api.sarbacane.com/v1`
- **Official documentation:** [List Campaigns](https://developers.sarbacane.com/campaigns/#list-campaigns)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `search` | query | `string` | no | Search text in campaign name or subject. |
| `state` | query | `string` | no | Campaign state selector: DRAFT, FINISH, ROUTING, or MODERATION. |
