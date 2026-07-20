# List Campaigns with Emailchef

Retrieves all campaigns from Emailchef.

## Endpoint

- **Method:** `GET`
- **Path:** `campaigns`
- **Base URL:** `https://app.emailchef.com/apps/api/v1`
- **Official documentation:** [List Campaigns](https://emailchef.com/integration/#/Campaigns/getCampaigns)

## Capabilities

This operation supports [pagination](../README.md#pagination) and [sorting](../README.md#sorting).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `status` | query | `string` | no | Optional campaign status filter. |
| `status1` | query | `string` | no | Optional first campaign status filter when using two statuses. |
| `status2` | query | `string` | no | Optional second campaign status filter. |
