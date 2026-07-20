# Remove Free Plan from Member with Memberstack

## Endpoint

- **Method:** `POST`
- **Path:** `/members/:id/remove-plan`
- **Base URL:** `https://admin.memberstack.com`
- **Official documentation:** [Remove Free Plan from Member](https://developers.memberstack.com/admin-rest-api/member-actions)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | Member ID (mem_...) to remove plan from. |
| `planId` | body | `string` | yes | Plan ID to remove from the member. |
