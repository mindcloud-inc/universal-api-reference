# Update name with Appwrite

Updates the name in your Appwrite project.

## Endpoint

- **Method:** `PUT`
- **Path:** `/teams/{teamId}`
- **Base URL:** `https://cloud.appwrite.io/v1`
- **Official documentation:** [Update name](https://appwrite.io/docs/references/cloud/server-rest/teams)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `teamId` | path | `string` | yes | Team ID. |
| `name` | body | `string` | yes | New team name. Max length: 128 chars. |
