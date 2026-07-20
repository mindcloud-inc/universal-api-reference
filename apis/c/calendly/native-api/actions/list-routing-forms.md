# List Routing Forms with Calendly

Retrieves routing forms from Calendly.

## Endpoint

- **Method:** `GET`
- **Path:** `/routing_forms`
- **Base URL:** `https://api.calendly.com`
- **Official documentation:** [List Routing Forms](https://developer.calendly.com/api-docs/9fe7334bec6ad-list-routing-forms)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `organization` | query | `list` | yes | Organization URI filter. Accepted values: `https://api.calendly.com/organizations/e684df12-9454-43ef-8fc4-2d0faa4ec21e`. |
| `sort` | query | `list` | no | Sort order for routing forms. Accepted values: `created_at:asc`, `created_at:desc`. |
