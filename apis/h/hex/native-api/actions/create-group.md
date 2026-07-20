# Create Group with Hex

## Endpoint

- **Method:** `POST`
- **Path:** `/groups`
- **Base URL:** `https://app.hex.tech/api/v1`
- **Official documentation:** [Create Group](https://learn.hex.tech/docs/api-integrations/api/reference#operation/CreateGroup)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `members.users[].id` | body | `string<string>` | no |
| `name` | body | `string` | yes |
