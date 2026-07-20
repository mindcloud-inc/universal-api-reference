# Remove Member from Group with ActiveTrail

Removes a member from a group in ActiveTrail.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/groups/:id/members/:memberId`
- **Base URL:** `https://webapi.mymarketing.co.il/api`
- **Official documentation:** [Remove Member from Group](https://webapi.mymarketing.co.il/api/docs/and/Api/DELETE-api-groups-id-members-memberId)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `number` | yes | Group id. Can be found using the account groups endpoint or in the UI. |
| `memberId` | path | `number` | yes | The member contact id to remove from the group. |
