# Microsoft Teams: List Joined Teams

Retrieves teams you've joined in Microsoft Teams.

```
GET https://connect.mindcloud.co/v1/universal/microsoftTeams/latest/actions/list-joined-teams
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Microsoft Teams `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/microsoftTeams/latest/actions/list-joined-teams?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/microsoftTeams/latest/actions/list-joined-teams?${params}`, {
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
      "classification": "string",
      "createdDateTime": "2026-05-07T12:00:00.000Z",
      "description": "string",
      "displayName": "Ava Chen",
      "id": "string",
      "isArchived": true,
      "specialization": "string",
      "tenantId": "string",
      "visibility": "string",
      "webUrl": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `classification` | string | Optional sensitivity or business classification label. |
| `createdDateTime` | date | Timestamp at which the team was created. |
| `description` | string | Optional description for the team. |
| `displayName` | string | Name of the team. |
| `id` | string | Unique identifier for the team. |
| `isArchived` | boolean | Whether the team is archived. |
| `specialization` | string | Team specialization value. |
| `tenantId` | string | Microsoft Entra tenant identifier. |
| `visibility` | string | Visibility of the team. |
| `webUrl` | string | Opaque Microsoft Teams client URL for the team. |

## Native endpoint

Through the native Microsoft Teams API, this operation is `GET /v1.0/me/joinedTeams` (base URL `https://graph.microsoft.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-joined-teams.md) for the provider-specific parameters and requirements.

