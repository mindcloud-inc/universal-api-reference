# Prerender.io: List Urls

Retrieves URLs from Prerender.io.

```
GET https://connect.mindcloud.co/v1/universal/prerenderio/latest/actions/get-v3-urls
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Prerender.io `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/prerenderio/latest/actions/get-v3-urls?connectionId=$CONNECTION_ID&limit=1&offset=1&wildcard=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "limit": "1",
  "offset": "1",
  "wildcard": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/prerenderio/latest/actions/get-v3-urls?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as query string parameters ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `adaptiveType` | string | no |  |
| `limit` | number | yes |  |
| `offset` | number | yes |  |
| `wildcard` | string | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "count": 1,
      "urls": [
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
| `count` | number |  |
| `urls` | array<object> |  |

## Native endpoint

Through the native Prerender.io API, this operation is `GET /v3/urls` (base URL `https://api.prerender.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-v3-urls.md) for the provider-specific parameters and requirements.

