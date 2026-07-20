# List Organization Members with Mem0

Retrieves organization members from Mem0.

## Endpoint

- **Method:** `GET`
- **Path:** `/api/v1/orgs/organizations/:org_id/members/`
- **Base URL:** `https://api.mem0.ai`
- **Official documentation:** [List Organization Members](https://docs.mem0.ai/api-reference/organization/get-org-members)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `org_id` | path | `string` | yes | Mem0 organization ID from the organization resource path. |
