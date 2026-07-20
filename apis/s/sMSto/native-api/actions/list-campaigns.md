# List Campaigns with SMS.to

Retrieves sent SMS campaigns from SMS.to.

## Endpoint

- **Method:** `GET`
- **Path:** `/v2/campaigns`
- **Base URL:** `https://api.sms.to`
- **Official documentation:** [List Campaigns](https://developers.sms.to/#2f2808c0-9b89-4cc9-8364-e1cae3f8a83f)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `limit` | query | `number` | no | The number of campaigns per page. |
| `page` | query | `number` | no | The page number. |
| `search` | query | `string` | no | Keywords to search for. |
