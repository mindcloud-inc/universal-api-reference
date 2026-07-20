# ScrapeGraphAI: Get SmartCrawler Status

Retrieves SmartCrawler task status from ScrapeGraphAI.

```
GET https://connect.mindcloud.co/v1/universal/scrapeGraphAI/latest/actions/get-smartcrawler-status
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ScrapeGraphAI `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/scrapeGraphAI/latest/actions/get-smartcrawler-status?connectionId=$CONNECTION_ID&taskId=74dd6738-66b1-4480-90b8-cb30df8ae2fb" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "taskId": "74dd6738-66b1-4480-90b8-cb30df8ae2fb"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/scrapeGraphAI/latest/actions/get-smartcrawler-status?${params}`, {
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
| `taskId` | string | yes | SmartCrawler task ID to retrieve. Example: `74dd6738-66b1-4480-90b8-cb30df8ae2fb`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "result": {},
      "status": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `result` | object |  |
| `status` | string |  |

## Native endpoint

Through the native ScrapeGraphAI API, this operation is `GET /crawl/:task_id` (base URL `https://api.scrapegraphai.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-smartcrawler-status.md) for the provider-specific parameters and requirements.

