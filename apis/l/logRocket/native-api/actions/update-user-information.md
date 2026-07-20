# Update User Information with LogRocket

## Endpoint

- **Method:** `PUT`
- **Path:** `/orgs/:orgId/apps/:projectId/users/:userId`
- **Base URL:** `https://api.logrocket.com/v1`
- **Official documentation:** [Update User Information](https://docs.logrocket.com/docs/user-identification-api)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `user_id` | path | `string` | yes | The LogRocket user ID to create or update. |
| `name` | body | `string` | no | Optional user name. LogRocket allows up to 1024 characters. |
| `email` | body | `string` | no | Optional user email. LogRocket allows up to 1024 characters. |
| `timestamp` | body | `number` | no | Optional Unix timestamp in milliseconds for the submitted user data. |
| `traits` | body | `object` | no | Optional object of user trait names and values. |
