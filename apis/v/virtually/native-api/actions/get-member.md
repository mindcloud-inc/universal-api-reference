# Get Member with Virtually

Retrieves a member from your Virtually workspace.

## Endpoint

- **Method:** `GET`
- **Path:** `/api/v2/orgs/:orgId/members/:memberId`
- **Base URL:** `https://app.tryvirtually.com`
- **Official documentation:** [Get Member](https://app.tryvirtually.com/api/docs#/Members/MembersController_findOne)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `memberId` | path | `string` | yes | The member ID. |
