# List Contacts with Freshdesk

Retrieves a list of contacts from Freshdesk.

## Endpoint

- **Method:** `GET`
- **Path:** `/contacts`
- **Base URL:** `https://{subdomain}.freshdesk.com/api/v2`
- **Official documentation:** [List Contacts](https://developers.freshdesk.com/api/#list_all_contacts)

## Capabilities

This operation supports [pagination](../README.md#pagination) and [filtering](../README.md#filtering).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `email` | query | `string` | no | — |
| `mobile` | query | `string` | no | — |
| `phone` | query | `string` | no | — |
| `company_id` | query | `list<number>` | no | — |
| `state` | query | `list<string>` | no | Accepted values: `blocked`, `deleted`, `unverified`, `verified`. |
| `contact_type` | query | `list<string>` | no | Accepted values: `contact`, `visitor`. |
| `updated_since` | query | `date` | no | — |
