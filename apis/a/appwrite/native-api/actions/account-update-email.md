# Update email with Appwrite

Updates the email in your Appwrite project.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/account/email`
- **Base URL:** `https://cloud.appwrite.io/v1`
- **Official documentation:** [Update email](https://appwrite.io/docs/references/cloud/server-rest/account)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `email` | body | `string` | yes | User email. |
| `password` | body | `string` | yes | User password. Must be at least 8 chars. |
