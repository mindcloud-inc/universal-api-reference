# List Meetings with IceCubes

## Endpoint

- **Method:** `GET`
- **Path:** `/meetings`
- **Base URL:** `https://icecubes.app/api/public`
- **Official documentation:** [List Meetings](https://icecubes.app/docs/api/rest)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `keyword` | query | `string` | no | Search by meeting title or keyword. |
| `participant` | query | `string` | no | Filter by participant email address. |
| `from_date` | query | `date` | no | Filter meetings from this date forward. |
| `to_date` | query | `date` | no | Filter meetings up to this date. |
| `scope` | query | `list` | no | Limit results to your personal meetings or the organization scope. Accepted values: `0`, `1`. |
| `tag` | query | `string` | no | Filter by tag name. |
| `hubspot_deal_id` | query | `string` | no | Filter by HubSpot deal ID. |
| `salesforce_opportunity_id` | query | `string` | no | Filter by Salesforce opportunity ID. |
