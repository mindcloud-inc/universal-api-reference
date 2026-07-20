# List Companies with CallRail

Retrieves companies from CallRail.

## Endpoint

- **Method:** `GET`
- **Path:** `/v3/a/:account_id/companies.json`
- **Base URL:** `https://api.callrail.com`
- **Official documentation:** [List Companies](https://apidocs.callrail.com/#listing-all-companies)

## Capabilities

This operation supports [pagination](../README.md#pagination), [filtering](../README.md#filtering), and [sorting](../README.md#sorting).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `account_id` | path | `string` | yes | The CallRail account ID. |
