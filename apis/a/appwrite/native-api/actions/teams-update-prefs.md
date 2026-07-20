# Update preferences with Appwrite

Updates the preferences in your Appwrite project.

## Endpoint

- **Method:** `PUT`
- **Path:** `/teams/{teamId}/prefs`
- **Base URL:** `https://cloud.appwrite.io/v1`
- **Official documentation:** [Update preferences](https://appwrite.io/docs/references/cloud/server-rest/teams)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `teamId` | path | `string` | yes | Team ID. |
| `prefs` | body | `object` | yes | Prefs key-value JSON object. |
