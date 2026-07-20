# Webcrawler API: Get Crawl Job URLs

Retrieves discovered URLs for a crawl job in Webcrawler API.

```
GET https://connect.mindcloud.co/v1/universal/webcrawlerAPI/latest/actions/get-crawl-job-urls
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Webcrawler API `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/webcrawlerAPI/latest/actions/get-crawl-job-urls?connectionId=$CONNECTION_ID&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/webcrawlerAPI/latest/actions/get-crawl-job-urls?${params}`, {
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
| `id` | string | yes | Crawl job ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "clusters": [
        {}
      ],
      "urls": [
        "https://example.com"
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `clusters` | array<object> | URL cluster summaries returned for the crawl job. |
| `urls` | array<string> | Discovered URLs returned for the crawl job. |

## Native endpoint

Through the native Webcrawler API API, this operation is `GET /v1/job/:id/urls` (base URL `https://api.webcrawlerapi.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-crawl-job-urls.md) for the provider-specific parameters and requirements.

