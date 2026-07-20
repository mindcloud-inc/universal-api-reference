# Fetch supported local jurisdictions with Middesk

Retrieves supported local jurisdictions from Middesk.

## Endpoint

- **Method:** `GET`
- **Path:** `/agent/jurisdictions`
- **Base URL:** `https://api.middesk.com/v1`
- **Official documentation:** [Fetch supported local jurisdictions](https://docs.middesk.com/docs/jurisdiction-registration-flow)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `state` | query | `string` | yes | US state abbreviation to fetch supported jurisdictions for. |
