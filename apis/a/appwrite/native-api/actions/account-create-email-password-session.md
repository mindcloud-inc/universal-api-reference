# Create email password session with Appwrite

Creates a new email password session in your Appwrite project.

## Endpoint

- **Method:** `POST`
- **Path:** `/account/sessions/email`
- **Base URL:** `https://cloud.appwrite.io/v1`
- **Official documentation:** [Create email password session](https://appwrite.io/docs/references/cloud/server-rest/account)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `email` | body | `string` | yes | User email. |
| `password` | body | `string` | yes | User password. Must be at least 8 chars. |
