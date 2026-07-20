# Renderly: Verify API Key

Verifies an API key in Renderly.

```
GET https://connect.mindcloud.co/v1/universal/renderly/latest/actions/verify-api-key
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Renderly `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/renderly/latest/actions/verify-api-key?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/renderly/latest/actions/verify-api-key?${params}`, {
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
      "apiKeyCreatedAt": "2026-05-07T12:00:00.000Z",
      "apiKeyLastUsed": "2026-05-07T12:00:00.000Z",
      "apiKeyPrefix": "string",
      "credits": 1,
      "email": "ava@example.com",
      "name": "Ava Chen",
      "userId": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `apiKeyCreatedAt` | date |  |
| `apiKeyLastUsed` | date |  |
| `apiKeyPrefix` | string |  |
| `credits` | number |  |
| `email` | string |  |
| `name` | string |  |
| `userId` | string |  |

## Native endpoint

Through the native Renderly API, this operation is `POST /auth/verify` (base URL `https://renderly.video/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/verify-api-key.md) for the provider-specific parameters and requirements.

