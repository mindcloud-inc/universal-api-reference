# CRUSH: List Tags



```
GET https://connect.mindcloud.co/v1/universal/cRUSH/latest/actions/list-tags
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a CRUSH `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/cRUSH/latest/actions/list-tags?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/cRUSH/latest/actions/list-tags?${params}`, {
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
      "createdAt": "2026-05-07T12:00:00.000Z",
      "id": "string",
      "name": "Ava Chen",
      "updatedAt": "2026-05-07T12:00:00.000Z",
      "userIds": [
        "string"
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `createdAt` | date | When the tag was created. |
| `id` | string | Unique tag identifier. |
| `name` | string | Tag name. |
| `updatedAt` | date | When the tag was last updated. |
| `userIds` | array<string> | User IDs that can access the tag. |

## Native endpoint

Through the native CRUSH API, this operation is `GET /aws/tags` (base URL `https://app.crushthememory.com/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-tags.md) for the provider-specific parameters and requirements.

