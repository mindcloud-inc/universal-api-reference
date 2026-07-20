# List Organization Memberships with Zendesk

Retrieves a list of organization memberships from Zendesk.

## Endpoint

- **Method:** `GET`
- **Path:** `/organization_memberships.json`
- **Base URL:** `https://{subdomain}.zendesk.com/api/v2`
- **Official documentation:** [List Organization Memberships](https://developer.zendesk.com/api-reference/ticketing/organizations/organization_memberships/#list-memberships)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `user_id` | query | `number` | no | Filter memberships by user ID. |
| `organization_id` | query | `number` | no | Filter memberships by organization ID. |
