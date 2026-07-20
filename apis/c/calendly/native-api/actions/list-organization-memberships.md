# List Organization Memberships with Calendly

Retrieves organization memberships from Calendly.

## Endpoint

- **Method:** `GET`
- **Path:** `/organization_memberships`
- **Base URL:** `https://api.calendly.com`
- **Official documentation:** [List Organization Memberships](https://developer.calendly.com/how-to-find-the-organization-or-user-uri)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `organization` | query | `list` | yes | Organization URI filter. Accepted values: `https://api.calendly.com/organizations/e684df12-9454-43ef-8fc4-2d0faa4ec21e`. |
