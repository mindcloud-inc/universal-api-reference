# Recallai: List Calendars

Retrieves calendars from Recallai.

```
GET https://connect.mindcloud.co/v1/universal/recallai/latest/actions/list-calendars
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Recallai `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/recallai/latest/actions/list-calendars?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/recallai/latest/actions/list-calendars?${params}`, {
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
      "id": "string",
      "metadata": {},
      "oauthClientId": "string",
      "oauthClientSecret": "string",
      "oauthEmail": "ava@example.com",
      "oauthRefreshToken": "string",
      "platform": "string",
      "platformEmail": "ava@example.com",
      "status": "string",
      "statusChanges": [
        {}
      ],
      "updatedAt": "string",
      "webhookUrl": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `createdAt` | string |  |
| `id` | string |  |
| `metadata` | object |  |
| `oauthClientId` | string |  |
| `oauthClientSecret` | string |  |
| `oauthEmail` | string |  |
| `oauthRefreshToken` | string |  |
| `platform` | string |  |
| `platformEmail` | string |  |
| `status` | string |  |
| `statusChanges` | array<object> |  |
| `updatedAt` | string |  |
| `webhookUrl` | string |  |

## Native endpoint

Through the native Recallai API, this operation is `GET /api/v2/calendars/` (base URL `https://{{credentials.workspaceRegion}}.recall.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-calendars.md) for the provider-specific parameters and requirements.

