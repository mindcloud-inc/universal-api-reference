# Netlify: List Site Build Hooks



```
GET https://connect.mindcloud.co/v1/universal/netlify/latest/actions/list-site-build-hooks
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Netlify `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/netlify/latest/actions/list-site-build-hooks?connectionId=$CONNECTION_ID&siteId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "siteId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/netlify/latest/actions/list-site-build-hooks?${params}`, {
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
| `siteId` | list<string> | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "branch": "string",
      "createdAt": "2026-05-07T12:00:00.000Z",
      "draft": true,
      "id": "string",
      "title": "string",
      "url": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `branch` | string | Target branch |
| `createdAt` | date | Creation timestamp |
| `draft` | boolean | Whether draft deploys are enabled |
| `id` | string | Build hook ID |
| `title` | string | Build hook title |
| `url` | string | Build hook URL |

## Native endpoint

Through the native Netlify API, this operation is `GET /sites/:site_id/build_hooks` (base URL `https://api.netlify.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-site-build-hooks.md) for the provider-specific parameters and requirements.

