# List Users with GatherUp

Retrieves a list of users from GatherUp.

## Endpoint

- **Method:** `POST`
- **Path:** `/user/managers/get`
- **Base URL:** `https://app.gatherup.com/api`
- **Official documentation:** [List Users](https://app.gatherup.com/api/doc/user/managers/get)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `email` | body | `string` | no | Search by email token. |
| `page` | body | `number` | no | Page. |
