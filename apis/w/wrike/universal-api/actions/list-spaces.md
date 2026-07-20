# Wrike: List Spaces

Finds spaces in Wrike.

```
GET https://connect.mindcloud.co/v1/universal/wrike/latest/actions/list-spaces
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Wrike `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/wrike/latest/actions/list-spaces?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/wrike/latest/actions/list-spaces?${params}`, {
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
      "accessType": "string",
      "archived": true,
      "avatarUrl": "https://example.com",
      "defaultProjectWorkflowId": "string",
      "defaultTaskWorkflowId": "string",
      "description": "string",
      "id": "string",
      "members": [
        {}
      ],
      "title": "string",
      "workScheduleId": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `accessType` | string |  |
| `archived` | boolean |  |
| `avatarUrl` | string |  |
| `defaultProjectWorkflowId` | string |  |
| `defaultTaskWorkflowId` | string |  |
| `description` | string |  |
| `id` | string |  |
| `members` | array<object> |  |
| `title` | string |  |
| `workScheduleId` | string |  |

## Native endpoint

Through the native Wrike API, this operation is `GET /spaces` (base URL `https://{{credentials.accessTokenRequest.host}}/api/v4`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-spaces.md) for the provider-specific parameters and requirements.

