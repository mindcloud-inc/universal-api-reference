# Timeular: Unarchive Folder

Unarchives an existing folder in your Timeular workspace.

```
PUT https://connect.mindcloud.co/v1/universal/timeular/latest/actions/unarchive-folder
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Timeular `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/timeular/latest/actions/unarchive-folder" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "folderId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/timeular/latest/actions/unarchive-folder', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "folderId": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `folderId` | string | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "id": "string",
      "members": [
        {
          "accessLevel": "string",
          "email": "ava@example.com",
          "id": "string",
          "name": "Ava Chen"
        }
      ],
      "name": "Ava Chen",
      "retiredMembers": [
        [
          "string"
        ]
      ],
      "status": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `id` | string |  |
| `members[].accessLevel` | string |  |
| `members[].email` | string |  |
| `members[].id` | string |  |
| `members[].name` | string |  |
| `name` | string |  |
| `retiredMembers[]` | array<string> |  |
| `status` | string |  |

## Native endpoint

Through the native Timeular API, this operation is `POST /api/v4/folders/:folderId/unarchive` (base URL `https://api.early.app`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/unarchive-folder.md) for the provider-specific parameters and requirements.

