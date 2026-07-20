# Openlayer: Get Profile

Retrieves your profile details from Openlayer.

```
GET https://connect.mindcloud.co/v1/universal/openlayer/latest/actions/get-profile
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Openlayer `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/openlayer/latest/actions/get-profile?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/openlayer/latest/actions/get-profile?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```



## Response

```json
{
  "success": true,
  "data": [
    {
      "confirmed": true,
      "dateCreated": "string",
      "email": "ava@example.com",
      "id": "string",
      "mfaEnabled": true,
      "name": "Ava Chen",
      "state": {
        "lastUsedWorkspaceId": "string"
      },
      "workspaces": [
        {
          "id": "string",
          "name": "Ava Chen",
          "slug": "string",
          "status": "string"
        }
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `confirmed` | boolean | Whether the user email is confirmed. |
| `dateCreated` | string | User creation timestamp. |
| `email` | string | User email. |
| `id` | string | User ID. |
| `mfaEnabled` | boolean | Whether MFA is enabled. |
| `name` | string | User name. |
| `state.lastUsedWorkspaceId` | string | Last used workspace ID. |
| `workspaces[].id` | string | Workspace ID. |
| `workspaces[].name` | string | Workspace name. |
| `workspaces[].slug` | string | Workspace slug. |
| `workspaces[].status` | string | Workspace status. |

## Native endpoint

Through the native Openlayer API, this operation is `GET /me` (base URL `https://api.openlayer.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-profile.md) for the provider-specific parameters and requirements.

