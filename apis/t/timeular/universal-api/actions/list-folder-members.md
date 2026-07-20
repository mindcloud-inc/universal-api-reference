# Timeular: List Folder Members

Retrieves members for a folder in your Timeular workspace.

```
GET https://connect.mindcloud.co/v1/universal/timeular/latest/actions/list-folder-members
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Timeular `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/timeular/latest/actions/list-folder-members?connectionId=$CONNECTION_ID&folderId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "folderId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/timeular/latest/actions/list-folder-members?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as query string parameters ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `folderId` | string | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "members": [
        {
          "accessLevel": "string",
          "email": "ava@example.com",
          "id": "string",
          "name": "Ava Chen"
        }
      ],
      "retiredMembers": [
        {
          "id": "string",
          "name": "Ava Chen"
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
| `members[].accessLevel` | string |  |
| `members[].email` | string |  |
| `members[].id` | string |  |
| `members[].name` | string |  |
| `retiredMembers[].id` | string |  |
| `retiredMembers[].name` | string |  |

## Native endpoint

Through the native Timeular API, this operation is `GET /api/v4/folders/:folderId/members` (base URL `https://api.early.app`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-folder-members.md) for the provider-specific parameters and requirements.

