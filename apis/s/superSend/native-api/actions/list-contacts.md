# List Contacts with SuperSend

Retrieves contacts from SuperSend.

## Endpoint

- **Method:** `GET`
- **Path:** `/contacts`
- **Base URL:** `https://api.supersend.io/v2`
- **Official documentation:** [List Contacts](https://docs.supersend.io/docs/contact)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `TeamId` | query | `string` | no | — |
| `CampaignId` | query | `string` | no | — |
| `limit` | query | `number` | no | Default: 50. Range: 1 to 100. |
| `offset` | query | `number` | no | Default: 0. Range: 0 to inf. |
| `search` | query | `string` | no | — |
| `interest` | query | `string` | no | Filter by contact status (interest). Comma-separated for multiple values. Values: interested, not_interested, meeting_request, meeting_booked, customer, future, follow_up. Use empty string or null to filter for contacts with no status. Send multiple values as a string separated by `,`. |
