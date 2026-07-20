# Get Paginated List of Contacts with Mihu AI

## Endpoint

- **Method:** `GET`
- **Path:** `/api/v1/contacts`
- **Base URL:** `https://{subdomain}.mindhunters.ai`
- **Official documentation:** [Get Paginated List of Contacts](https://developers.mihu.ai/api-reference/contacts/get-paginated-list-of-contacts)

## Capabilities

This operation supports [pagination](../README.md#pagination) and [filtering](../README.md#filtering).

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `page` | query | `number` | no |
| `per_page` | query | `number` | no |
| `search` | query | `string` | no |
| `status` | query | `string` | no |
