# Prerender.io: List Seo Urls

Retrieves SEO URLs from Prerender.io.

```
GET https://connect.mindcloud.co/v1/universal/prerenderio/latest/actions/get-v3-seo-urls
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Prerender.io `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/prerenderio/latest/actions/get-v3-seo-urls?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/prerenderio/latest/actions/get-v3-seo-urls?${params}`, {
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
| `adaptive_type` | string | no |  |
| `domain` | string | no |  |
| `domainId` | string | no |  |
| `page` | number | no |  |
| `pageSize` | number | no |  |
| `q` | string | no |  |
| `sort` | string | no |  |
| `sortDirection` | string | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
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
| `urls` | array<object> |  |

## Native endpoint

Through the native Prerender.io API, this operation is `GET /v3/seo/urls` (base URL `https://api.prerender.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-v3-seo-urls.md) for the provider-specific parameters and requirements.

