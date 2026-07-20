# Update Member with Virtually

Updates an existing member in Virtually.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/api/v2/orgs/:orgId/members/:memberId`
- **Base URL:** `https://app.tryvirtually.com`
- **Official documentation:** [Update Member](https://app.tryvirtually.com/api/docs#/Members/MembersController_update)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `memberId` | path | `string` | yes | The member ID. |
| `name` | body | `string` | no | The member name. |
| `email` | body | `string` | no | The member email address. |
| `tagIds[]` | body | `array<string>` | no | The tag IDs to assign to the member. |
| `properties` | body | `object` | no | Additional member properties. |
| `status` | body | `string` | no | The member status. |
