# Daytona: Get Current API Key

Retrieves the current API key details from Daytona.

```
GET https://connect.mindcloud.co/v1/universal/daytona/latest/actions/get-current-api-key
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Daytona `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/daytona/latest/actions/get-current-api-key?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/daytona/latest/actions/get-current-api-key?${params}`, {
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
      "expiresAt": "2026-05-07T12:00:00.000Z",
      "lastUsedAt": "2026-05-07T12:00:00.000Z",
      "name": "Ava Chen",
      "permissions": [
        "string"
      ],
      "userId": "string",
      "value": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `createdAt` | date |  |
| `expiresAt` | date |  |
| `lastUsedAt` | date |  |
| `name` | string |  |
| `permissions` | array<string> |  |
| `userId` | string |  |
| `value` | string | Masked API key value returned by Daytona. |

## Native endpoint

Through the native Daytona API, this operation is `GET /api-keys/current` (base URL `https://app.daytona.io/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-current-api-key.md) for the provider-specific parameters and requirements.

