# Kite Suite: List Teams



```
GET https://connect.mindcloud.co/v1/universal/kiteSuiteCustom/latest/actions/list-teams
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Kite Suite `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/kiteSuiteCustom/latest/actions/list-teams?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/kiteSuiteCustom/latest/actions/list-teams?${params}`, {
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
      "_id": "string",
      "createdAt": "string",
      "createdBy": "string",
      "description": "string",
      "isTrashed": true,
      "members": [
        "string"
      ],
      "name": "Ava Chen",
      "updatedAt": "string",
      "workspace": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `_id` | string | ID of the Team |
| `createdAt` | string | Team creation date |
| `createdBy` | string | User ID of creator |
| `description` | string | Description of the Team |
| `isTrashed` | boolean | Trash status of the Team |
| `members` | array<string> | List of team members (user references) |
| `name` | string | Name of the Team |
| `updatedAt` | string | Last update date |
| `workspace` | string | Workspace ID this team belongs to |

## Native endpoint

Through the native Kite Suite API, this operation is `GET /api/v1/team` (base URL `https://api.kitesuite.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-teams.md) for the provider-specific parameters and requirements.

