# Cursion: Create Site

Creates a new site in Cursion.

```
POST https://connect.mindcloud.co/v1/universal/cursion/latest/actions/create-site
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Cursion `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/cursion/latest/actions/create-site" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "siteUrl": "https://example.com"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/cursion/latest/actions/create-site', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "siteUrl": "https://example.com"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `siteUrl` | string | yes | The site URL to monitor. |

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

Through the native Cursion API, this operation is `POST /site` (base URL `https://api.cursion.dev/v1/ops`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-site.md) for the provider-specific parameters and requirements.

