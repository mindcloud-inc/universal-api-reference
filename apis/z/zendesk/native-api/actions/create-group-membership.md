# Create Group Membership with Zendesk

Creates a new group membership in Zendesk.

## Endpoint

- **Method:** `POST`
- **Path:** `/group_memberships.json`
- **Base URL:** `https://{subdomain}.zendesk.com/api/v2`
- **Official documentation:** [Create Group Membership](https://developer.zendesk.com/api-reference/ticketing/groups/group_memberships/#create-membership)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `group_membership.user_id` | body | `number` | yes | Group membership user ID |
| `group_membership.group_id` | body | `number` | yes | Group membership group ID |
