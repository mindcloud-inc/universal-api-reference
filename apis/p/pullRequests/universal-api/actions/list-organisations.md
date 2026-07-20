# 24 Pull Requests: List Organisations

Retrieves organisations from 24 Pull Requests.

```
GET https://connect.mindcloud.co/v1/universal/pullRequests/latest/actions/list-organisations
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a 24 Pull Requests `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/pullRequests/latest/actions/list-organisations?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/pullRequests/latest/actions/list-organisations?${params}`, {
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
      "avatar_url": "https://example.com",
      "link": "https://example.com",
      "login": "string",
      "users": [
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
| `avatar_url` | string | Organisation avatar URL. |
| `link` | string | Organisation page URL. |
| `login` | string | Organisation login. |
| `users` | array<object> | Organisation users. |

## Native endpoint

Through the native 24 Pull Requests API, this operation is `GET /organisations.json` (base URL `https://24pullrequests.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-organisations.md) for the provider-specific parameters and requirements.

