# List Team Members with Pinghome

Retrieves team members from Pinghome.

## Endpoint

- **Method:** `GET`
- **Path:** `/customer-query/v1/team/:id/members`
- **Base URL:** `https://api.pinghome.io`
- **Official documentation:** [List Team Members](https://docs.pinghome.io/customer-account-management/team-organization-and-role-setup/get-team-members/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | The unique ID of the team. |
