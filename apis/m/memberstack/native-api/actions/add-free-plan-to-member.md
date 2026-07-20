# Add Free Plan to Member with Memberstack

## Endpoint

- **Method:** `POST`
- **Path:** `/members/:id/add-plan`
- **Base URL:** `https://admin.memberstack.com`
- **Official documentation:** [Add Free Plan to Member](https://developers.memberstack.com/admin-rest-api/member-actions)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | Member ID (mem_...) to grant plan access. |
| `planId` | body | `string` | yes | Plan ID to add to the member. |
