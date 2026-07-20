# Anonymize User with Discourse

Anonymizes an existing user in Discourse.

## Endpoint

- **Method:** `PUT`
- **Path:** `/admin/users/:id/anonymize.json`
- **Base URL:** `https://mindcloud.discourse.group`
- **Official documentation:** [Anonymize User](https://docs.discourse.org/#tag/Users/operation/anonymizeUser)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `number` | yes | User id. |
