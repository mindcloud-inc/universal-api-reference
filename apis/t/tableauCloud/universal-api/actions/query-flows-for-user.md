# Tableau Cloud: Query Flows for User

Retrieves a user's flows from Tableau Cloud.

```
GET https://connect.mindcloud.co/v1/universal/tableauCloud/latest/actions/query-flows-for-user
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Tableau Cloud `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/tableauCloud/latest/actions/query-flows-for-user?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/tableauCloud/latest/actions/query-flows-for-user?${params}`, {
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
      "createdAt": "string",
      "description": "string",
      "fileType": "string",
      "id": "string",
      "name": "Ava Chen",
      "updatedAt": "string",
      "webpageUrl": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `createdAt` | string | Creation timestamp. |
| `description` | string | Flow description. |
| `fileType` | string | Flow file type. |
| `id` | string | Flow ID. |
| `name` | string | Flow name. |
| `updatedAt` | string | Last update timestamp. |
| `webpageUrl` | string | Flow web URL. |

## Native endpoint

Through the native Tableau Cloud API, this operation is `GET /sites/site-id/users/user-id/flows` (base URL `https://us-east-1.online.tableau.com/api/3.28`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/query-flows-for-user.md) for the provider-specific parameters and requirements.

