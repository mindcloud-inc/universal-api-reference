# List Companies with Freshdesk

Retrieves a list of companies from Freshdesk.

## Endpoint

- **Method:** `GET`
- **Path:** `/companies`
- **Base URL:** `https://{subdomain}.freshdesk.com/api/v2`
- **Official documentation:** [List Companies](https://developers.freshdesk.com/api/#list_all_companies)

## Capabilities

This operation supports [pagination](../README.md#pagination) and [filtering](../README.md#filtering).

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `updated_since` | query | `date` | no |
