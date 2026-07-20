# Create Remote User Login with Knack

## Endpoint

- **Method:** `POST`
- **Path:** `/applications/{applicationId}/session`
- **Base URL:** `https://api.knack.com/v1`
- **Official documentation:** [Create Remote User Login](https://docs.knack.com/reference/remote-user-logins)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `email` | body | `string` | yes | Email address for a non-SSO Knack user account. |
| `password` | body | `string` | yes | Password for the non-SSO Knack user account. |
