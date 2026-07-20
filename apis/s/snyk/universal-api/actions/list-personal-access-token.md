# Snyk: List Personal Access Tokens

Retrieves personal access tokens for the current Snyk user.

```
GET https://connect.mindcloud.co/v1/universal/snyk/latest/actions/list-personal-access-token
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Snyk `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/snyk/latest/actions/list-personal-access-token?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/snyk/latest/actions/list-personal-access-token?${params}`, {
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
      "data": [
        {}
      ],
      "jsonapi": {},
      "meta": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data` | array<object> | Personal access tokens visible to the current user. |
| `jsonapi` | object | JSON:API metadata. |
| `meta` | object | Token policy metadata returned by Snyk. |

## Native endpoint

Through the native Snyk API, this operation is `GET /self/personal_access_tokens` (base URL `https://api.snyk.io/rest`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-personal-access-token.md) for the provider-specific parameters and requirements.

