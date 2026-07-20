# Delete Member with PassKit Membership

Deletes an existing member from PassKit Membership.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/members/member`
- **Base URL:** `https://api.pub2.passkit.io`
- **Official documentation:** [Delete Member](https://help.passkit.com/en/articles/4134575-editing-members-through-the-api)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | body | `string` | yes | PassKit member id to delete. |
