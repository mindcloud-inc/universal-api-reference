# List Groups with Frontegg

Finds user groups for a Frontegg account.

## Endpoint

- **Method:** `GET`
- **Path:** `/identity/resources/groups/v1`
- **Base URL:** `https://api.frontegg.com`
- **Official documentation:** [List Groups](https://developers.frontegg.com/ciam/api/identity/user-groups)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `_groupsRelations` | query | `list` | no | Include related roles and/or users. |
