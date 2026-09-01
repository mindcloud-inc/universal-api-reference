# List Center Membership Details with Zenoti

## Endpoint

- **Method:** `GET`
- **Path:** `centers/:centerId/members`
- **Base URL:** `https://api.zenoti.com/v1/`
- **Official documentation:** [List Center Membership Details](https://docs.zenoti.com/reference/retrieve-the-details-of-all-the-members-of-a-center)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `centerId` | path | `list` | no | — |
| `status` | query | `list` | no | — |
| `created_date` | query | `date` | no | — |
| `last_updated_date` | query | `date` | no | — |
| `returnOnlyTotal` | query | `boolean` | no | Format: `toggle`. |
