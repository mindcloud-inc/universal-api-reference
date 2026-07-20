# Cursor: API Key Info



```
GET https://connect.mindcloud.co/v1/universal/cursor/latest/actions/api-key-info
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Cursor `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/cursor/latest/actions/api-key-info?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/cursor/latest/actions/api-key-info?${params}`, {
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
      "apiKeyName": "Ava Chen",
      "createdAt": "2026-05-07T12:00:00.000Z",
      "userEmail": "ava@example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `apiKeyName` | string | The name of the API key. |
| `createdAt` | date | When the API key was created. |
| `userEmail` | string | Email address of the API key owner, when available. |

## Native endpoint

Through the native Cursor API, this operation is `GET /v0/me` (base URL `https://api.cursor.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/api-key-info.md) for the provider-specific parameters and requirements.

