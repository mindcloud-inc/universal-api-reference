# Get User Activity with Qntrl

Retrieves user activity from Qntrl.

## Endpoint

- **Method:** `GET`
- **Path:** `/[:org_id]/user/activity/[:user_id]`
- **Base URL:** `https://coreapi.qntrl.com/blueprint/api`
- **Official documentation:** [Get User Activity](https://core.qntrl.com/apidoc.html#useractivity)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `org_id` | path | `string` | no | Qntrl organization ID. |
| `user_id` | path | `string` | no | Qntrl user ID. |
