# Add Organization Member with Mem0

Adds a member to an organization in Mem0.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/v1/orgs/organizations/:org_id/members/`
- **Base URL:** `https://api.mem0.ai`
- **Official documentation:** [Add Organization Member](https://docs.mem0.ai/api-reference/organization/add-org-member)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `org_id` | path | `string` | yes | Mem0 organization ID from the organization resource path. |
