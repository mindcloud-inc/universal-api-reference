# SonarQube: List User Tokens

Retrieves user tokens from SonarQube.

```
GET https://connect.mindcloud.co/v1/universal/sonarQube/latest/actions/list-user-tokens
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a SonarQube `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/sonarQube/latest/actions/list-user-tokens?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/sonarQube/latest/actions/list-user-tokens?${params}`, {
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
      "login": "string",
      "userTokens": [
        {}
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `login` | string |  |
| `userTokens` | array<object> |  |

## Native endpoint

Through the native SonarQube API, this operation is `GET /api/user_tokens/search` (base URL `https://sonarcloud.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-user-tokens.md) for the provider-specific parameters and requirements.

