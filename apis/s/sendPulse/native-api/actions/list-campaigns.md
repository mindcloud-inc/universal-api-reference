# List Campaigns with SendPulse

Retrieves a list of campaigns from SendPulse.

## Endpoint

- **Method:** `GET`
- **Path:** `/campaigns`
- **Base URL:** `https://api.sendpulse.com`
- **Official documentation:** [List Campaigns](https://sendpulse.com/integrations/api/bulk-email#campaigns-list)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `limit` | query | `number` | no | Maximum number of campaigns to return. |
| `offset` | query | `number` | no | Number of campaigns to skip before returning results. |
| `status` | query | `string` | no | Filter campaigns by status. |
