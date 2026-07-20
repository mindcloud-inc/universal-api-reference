# Grok: Get API Key

Retrieves the authenticated API key from Grok.

```
GET https://connect.mindcloud.co/v1/universal/grok/latest/actions/get-api-key
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Grok `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/grok/latest/actions/get-api-key?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/grok/latest/actions/get-api-key?${params}`, {
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
      "acls": [
        "string"
      ],
      "apiKeyBlocked": true,
      "apiKeyDisabled": true,
      "apiKeyId": "string",
      "createTime": "string",
      "modifiedBy": "string",
      "modifyTime": "string",
      "name": "Ava Chen",
      "redactedApiKey": "string",
      "teamBlocked": true,
      "teamId": "string",
      "userId": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `acls` | array<string> | Access control entries granted to the API key. |
| `apiKeyBlocked` | boolean | Whether the API key is blocked. |
| `apiKeyDisabled` | boolean | Whether the API key is disabled. |
| `apiKeyId` | string | Unique API key identifier. |
| `createTime` | string | Creation timestamp returned by xAI. |
| `modifiedBy` | string | User ID that last modified the API key. |
| `modifyTime` | string | Last modification timestamp returned by xAI. |
| `name` | string | Display name of the API key. |
| `redactedApiKey` | string | Redacted display value for the current API key. |
| `teamBlocked` | boolean | Whether the owning team is blocked. |
| `teamId` | string | Team ID associated with the API key. |
| `userId` | string | User ID that owns the API key. |

## Native endpoint

Through the native Grok API, this operation is `GET /v1/api-key` (base URL `https://api.x.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-api-key.md) for the provider-specific parameters and requirements.

