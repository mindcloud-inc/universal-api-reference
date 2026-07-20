# Timeular: List Folders

Retrieves folders from your Timeular workspace.

```
GET https://connect.mindcloud.co/v1/universal/timeular/latest/actions/list-folders
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Timeular `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/timeular/latest/actions/list-folders?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/timeular/latest/actions/list-folders?${params}`, {
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
      "folders": [
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
            {
              "id": "string",
              "name": "Ava Chen"
            }
          ],
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
| `folders[].id` | string |  |
| `folders[].members[].accessLevel` | string |  |
| `folders[].members[].email` | string |  |
| `folders[].members[].id` | string |  |
| `folders[].members[].name` | string |  |
| `folders[].name` | string |  |
| `folders[].retiredMembers[].id` | string |  |
| `folders[].retiredMembers[].name` | string |  |
| `folders[].status` | string |  |

## Native endpoint

Through the native Timeular API, this operation is `GET /api/v4/folders` (base URL `https://api.early.app`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-folders.md) for the provider-specific parameters and requirements.

