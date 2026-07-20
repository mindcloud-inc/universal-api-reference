# Cloudflare Browser Run: Get Crawl Result

Retrieves crawl job results from Cloudflare Browser Run.

```
GET https://connect.mindcloud.co/v1/universal/cloudflareBrowserRun/latest/actions/get-crawl-result
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Cloudflare Browser Run `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/cloudflareBrowserRun/latest/actions/get-crawl-result?connectionId=$CONNECTION_ID&jobId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "jobId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/cloudflareBrowserRun/latest/actions/get-crawl-result?${params}`, {
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
| `jobId` | string | yes | Crawl job ID returned by Create Crawl Job. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "result": {
        "browserSecondsUsed": 1,
        "finished": 1,
        "id": "string",
        "records": [
          {}
        ],
        "skipped": 1,
        "status": "string",
        "total": 1
      },
      "success": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `result` | object |  |
| `result.browserSecondsUsed` | number |  |
| `result.finished` | number |  |
| `result.id` | string |  |
| `result.records` | array<object> |  |
| `result.skipped` | number |  |
| `result.status` | string |  |
| `result.total` | number |  |
| `success` | boolean |  |

## Native endpoint

Through the native Cloudflare Browser Run API, this operation is `GET /accounts/:accountId/browser-rendering/crawl/:jobId` (base URL `https://api.cloudflare.com/client/v4`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-crawl-result.md) for the provider-specific parameters and requirements.

