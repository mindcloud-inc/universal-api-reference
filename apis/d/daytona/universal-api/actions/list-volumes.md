# Daytona: List Volumes

Retrieves all volumes from Daytona.

```
GET https://connect.mindcloud.co/v1/universal/daytona/latest/actions/list-volumes
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Daytona `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/daytona/latest/actions/list-volumes?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/daytona/latest/actions/list-volumes?${params}`, {
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
      "errorReason": "string",
      "id": "string",
      "lastUsedAt": "2026-05-07T12:00:00.000Z",
      "name": "Ava Chen",
      "organizationId": "string",
      "state": "string",
      "updatedAt": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `createdAt` | date |  |
| `errorReason` | string |  |
| `id` | string |  |
| `lastUsedAt` | date |  |
| `name` | string |  |
| `organizationId` | string |  |
| `state` | string |  |
| `updatedAt` | date |  |

## Native endpoint

Through the native Daytona API, this operation is `GET /volumes` (base URL `https://app.daytona.io/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-volumes.md) for the provider-specific parameters and requirements.

