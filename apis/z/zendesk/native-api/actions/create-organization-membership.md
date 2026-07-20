# Create Organization Membership with Zendesk

Creates a new organization membership in Zendesk.

## Endpoint

- **Method:** `POST`
- **Path:** `/organization_memberships.json`
- **Base URL:** `https://{subdomain}.zendesk.com/api/v2`
- **Official documentation:** [Create Organization Membership](https://developer.zendesk.com/api-reference/ticketing/organizations/organization_memberships/#create-membership)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `organization_membership.user_id` | body | `number` | yes | Organization membership user ID |
| `organization_membership.organization_id` | body | `number` | yes | Organization membership organization ID |
