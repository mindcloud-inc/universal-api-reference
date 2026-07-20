# Update Current User with TMetric

## Endpoint

- **Method:** `PATCH`
- **Path:** `/user`
- **Base URL:** `https://app.tmetric.com/api/v3`
- **Official documentation:** [Update Current User](https://app.tmetric.com/api-docs/#/User/patch-user)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `activeAccountId` | body | `number` | no | Workspace to make active for the current user. |
| `name` | body | `string` | no | Updated user name. |
