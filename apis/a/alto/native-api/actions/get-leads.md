# Get Leads with Alto

Retrieves lead records from your Alto account.

## Endpoint

- **Method:** `GET`
- **Path:** `/leads`
- **Base URL:** `https://api.alto.zoopladev.co.uk`
- **Official documentation:** [Get Leads](https://developers.vebraalto.com/api)

## Capabilities

This operation supports [pagination](../README.md#pagination) and [filtering](../README.md#filtering).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `lead-status` | query | `string` | no | Lead status filter. |
| `modified-from` | query | `date` | no | Return leads modified on or after this date. |
| `modified-to` | query | `date` | no | Return leads modified on or before this date. |
