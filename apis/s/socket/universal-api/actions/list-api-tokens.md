# Socket: List API Tokens

Retrieves organization API tokens from Socket.

```
GET https://connect.mindcloud.co/v1/universal/socket/latest/actions/list-api-tokens
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Socket `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/socket/latest/actions/list-api-tokens?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/socket/latest/actions/list-api-tokens?${params}`, {
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
      "nextPage": 1,
      "tokens": [
        {
          "committers": [
            {}
          ],
          "createdAt": "2026-05-07T12:00:00.000Z",
          "createdBy": "string",
          "groupUuid": "string",
          "hash": "string",
          "id": "string",
          "lastUsedAt": "2026-05-07T12:00:00.000Z",
          "maxQuota": 1,
          "name": "Ava Chen",
          "scopes": [
            "string"
          ],
          "token": "string",
          "visibility": "string"
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
| `nextPage` | number |  |
| `tokens` | array<object> |  |
| `tokens[]` | object | API Token response schema |
| `tokens[].committers` | array<object> |  |
| `tokens[].committers[]` | object | Committer information associated with the API Token |
| `tokens[].createdAt` | date | Timestamp when the API Token was created |
| `tokens[].createdBy` | string | ID of the Socket user who created the API Token |
| `tokens[].groupUuid` | string | The stable group UUID that remains constant across token rotations |
| `tokens[].hash` | string | SRI-format hash of the token (e.g., sha512-base64hash). Null for tokens created before hash column was added. |
| `tokens[].id` | string | The ID of the API Token |
| `tokens[].lastUsedAt` | date | Timestamp when the API Token was last used |
| `tokens[].maxQuota` | number | Maximum number of API calls allowed per month |
| `tokens[].name` | string | Name for the API Token |
| `tokens[].scopes` | array<string> |  |
| `tokens[].token` | string | The token of the API Token (redacted or omitted) |
| `tokens[].visibility` | string | The visibility of the API Token. Warning: this field is deprecated and will be removed in the future. |

## Native endpoint

Through the native Socket API, this operation is `GET /orgs/:org_slug/api-tokens` (base URL `https://api.socket.dev/v0`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-api-tokens.md) for the provider-specific parameters and requirements.

