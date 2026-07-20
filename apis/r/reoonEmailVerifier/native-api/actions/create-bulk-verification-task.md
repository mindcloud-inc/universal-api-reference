# Create Bulk Verification Task with Reoon Email Verifier

## Endpoint

- **Method:** `POST`
- **Path:** `/create-bulk-verification-task/`
- **Base URL:** `https://emailverifier.reoon.com/api/v1`
- **Official documentation:** [Create Bulk Verification Task](https://www.reoon.com/articles/api-documentation-of-reoon-email-verifier/)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |
| `Content-Type` | `application/json` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `name` | body | `string` | no | Optional task name shown in Reoon. Maximum length: 25. |
| `emails` | body | `object<string>` | yes | Array of email addresses to verify in bulk. Serialized as a JSON array for Reoon bulk task creation. Send multiple values as a array. |
