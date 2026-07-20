# List Portal Users, Client Users, And Contacts with Zoho Projects

Retrieves portal users, client users, and contacts from Zoho Projects.

## Endpoint

- **Method:** `GET`
- **Path:** `/portal/[:PORTALID]/users`
- **Base URL:** `https://projectsapi.zoho.com/api/v3`
- **Official documentation:** [List Portal Users, Client Users, And Contacts](https://projectsapi.zoho.com/api-docs#users_get-all-portal-users-client-users-and-contacts)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `PORTALID` | path | `string` | yes | Zoho Projects portal ID. |
| `type` | query | `number` | no | User type selector. |
| `view_type` | query | `string` | no | User activity view type. |
| `sort` | query | `string` | no | Sort order. |
| `ids` | query | `string` | no | Comma-separated user IDs. |
| `company_ids` | query | `string` | no | Comma-separated customer IDs. |
| `view` | query | `string` | no | Data view type. |
| `filter` | query | `string` | no | Raw JSON filter object from Zoho Projects. |
