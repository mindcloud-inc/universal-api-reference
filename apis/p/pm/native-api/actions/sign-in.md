# Sign In with 5pm

Signs in to 5pm and returns a session ID.

## Endpoint

- **Method:** `GET`
- **Path:** `/service/get/authentication/signIn`
- **Base URL:** `{workspaceUrl}/api/v2`
- **Official documentation:** [Sign In](https://www.5pmweb.com/help/api_docs.php)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `login` | query | `string` | yes | 5pm login used for the authentication signIn call. |
