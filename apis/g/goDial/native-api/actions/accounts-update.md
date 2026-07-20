# Update User with GoDial

Updates an existing user in GoDial.

## Endpoint

- **Method:** `PUT`
- **Path:** `/externals/accounts/[:id]/update`
- **Base URL:** `https://enterprise.godial.cc/meta/api`
- **Official documentation:** [Update User](https://godial.stoplight.io/docs/godial/b3A6MzAzMTY1OA-accounts-update)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | Account ID. |
| `role` | body | `string` | yes | Provide role of the User. Accepted values: teammanager, submanager, agent |
| `teamsId[]` | body | `array<string>` | yes | Provide teamsId for the User as a JSON array, e.g. ["teamId1"] |
