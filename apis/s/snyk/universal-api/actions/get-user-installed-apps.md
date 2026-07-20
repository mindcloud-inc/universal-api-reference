# Snyk: List User Installed Apps

Retrieves installed apps for the current Snyk user.

```
GET https://connect.mindcloud.co/v1/universal/snyk/latest/actions/get-user-installed-apps
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Snyk `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/snyk/latest/actions/get-user-installed-apps?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/snyk/latest/actions/get-user-installed-apps?${params}`, {
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
      "links": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data` | array<object> | Apps that can act on behalf of the current user. |
| `jsonapi` | object | JSON:API metadata. |
| `links` | object | Pagination and self links. |

## Native endpoint

Through the native Snyk API, this operation is `GET /self/apps` (base URL `https://api.snyk.io/rest`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-user-installed-apps.md) for the provider-specific parameters and requirements.

