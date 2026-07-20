# Update token with Appwrite

Updates the token in your Appwrite project.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/tokens/{tokenId}`
- **Base URL:** `https://cloud.appwrite.io/v1`
- **Official documentation:** [Update token](https://appwrite.io/docs/references/cloud/server-rest/tokens)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `tokenId` | path | `string` | yes | Token unique ID. |
| `expire` | body | `string` | no | File token expiry date |
