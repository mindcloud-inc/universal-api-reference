# Zoho Sprints: List Workspaces

Retrieves workspaces from Zoho Sprints.

```
GET https://connect.mindcloud.co/v1/universal/zohoSprints/latest/actions/list-workspaces
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Zoho Sprints `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/zohoSprints/latest/actions/list-workspaces?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/zohoSprints/latest/actions/list-workspaces?${params}`, {
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
      "baseURL": "https://example.com",
      "createTeamAllowed": true,
      "defaultPortalId": "string",
      "myTeamId": "string",
      "ownerTeamIds": [
        "string"
      ],
      "portals": [
        {}
      ],
      "status": "string",
      "userDisplayName": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `baseURL` | string | Base Zoho Sprints URL returned by the workspace lookup. |
| `createTeamAllowed` | boolean | Whether the authenticated user can create new teams or workspaces. |
| `defaultPortalId` | string | Default portal identifier returned by Zoho Sprints for the authenticated user. |
| `myTeamId` | string | Primary team identifier for the authenticated user. |
| `ownerTeamIds` | array<string> | Workspace team identifiers associated with the authenticated user. |
| `portals` | array<object> | Workspace portal summaries visible to the authenticated user. |
| `status` | string | Zoho Sprints API status string for the workspace lookup. |
| `userDisplayName` | object | Map of user identifiers to display names returned by the workspace lookup. |

## Native endpoint

Through the native Zoho Sprints API, this operation is `GET /teams/` (base URL `https://sprintsapi.zoho.com/zsapi`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-workspaces.md) for the provider-specific parameters and requirements.

