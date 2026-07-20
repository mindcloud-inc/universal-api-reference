# Printful: List OAuth Scopes

Retrieves available OAuth scopes for a Printful token.

```
GET https://connect.mindcloud.co/v1/universal/printful/latest/actions/list-o-auth-scopes
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Printful `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/printful/latest/actions/list-o-auth-scopes?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/printful/latest/actions/list-o-auth-scopes?${params}`, {
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
      "scope": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `scope` | string |  |

## Native endpoint

Through the native Printful API, this operation is `GET /oauth/scopes` (base URL `https://api.printful.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-o-auth-scopes.md) for the provider-specific parameters and requirements.

