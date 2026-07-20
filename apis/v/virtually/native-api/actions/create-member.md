# Create Member with Virtually

Creates a new member in Virtually.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/v2/orgs/:orgId/members`
- **Base URL:** `https://app.tryvirtually.com`
- **Official documentation:** [Create Member](https://app.tryvirtually.com/api/docs#/Members/MembersController_create)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `name` | body | `string` | yes | The member name. |
| `email` | body | `string` | yes | The member email address. |
| `tagIds[]` | body | `array<string>` | yes | The tag IDs to assign to the member. |
| `role` | body | `string` | yes | The member role. |
| `properties` | body | `object` | yes | Additional member properties. |
| `status` | body | `string` | yes | The member status. |
