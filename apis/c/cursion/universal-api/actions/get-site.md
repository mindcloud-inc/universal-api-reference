# Cursion: Get Site

Retrieves an existing site from Cursion.

```
GET https://connect.mindcloud.co/v1/universal/cursion/latest/actions/get-site
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Cursion `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/cursion/latest/actions/get-site?connectionId=$CONNECTION_ID&siteId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "siteId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/cursion/latest/actions/get-site?${params}`, {
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
| `siteId` | string | yes | The site identifier. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "account": "string",
      "id": "string",
      "info": {},
      "site_url": "https://example.com",
      "tags": [
        "string"
      ],
      "time_crawl_completed": "string",
      "time_crawl_started": "string",
      "time_created": "string",
      "user": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `account` | string |  |
| `id` | string |  |
| `info` | object |  |
| `site_url` | string |  |
| `tags` | array<string> |  |
| `time_crawl_completed` | string |  |
| `time_crawl_started` | string |  |
| `time_created` | string |  |
| `user` | string |  |

## Native endpoint

Through the native Cursion API, this operation is `GET /site/{{siteId}}` (base URL `https://api.cursion.dev/v1/ops`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-site.md) for the provider-specific parameters and requirements.

