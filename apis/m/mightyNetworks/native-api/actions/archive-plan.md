# Archive Plan with Mighty Networks

Archives a plan in Mighty Networks, canceling subscriptions and revoking access.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/networks/:network_id/plans/:id/`
- **Base URL:** `https://api.mn.co/admin/v1`
- **Official documentation:** [Archive Plan](https://docs.mightynetworks.com/api-reference/plans/archive-a-plan-this-will-cancel-all-associated-subscriptions-and-revoke-access)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `network_id` | path | `string` | yes | The Mighty Networks network ID. |
| `id` | path | `number` | yes | The ID of the plan to archive. |
