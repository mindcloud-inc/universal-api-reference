# ScraperAPI: Create Async Batch Jobs

Creates async batch scraping jobs in ScraperAPI.

```
POST https://connect.mindcloud.co/v1/universal/scraperAPI/latest/actions/create-async-batch-jobs
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ScraperAPI `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/scraperAPI/latest/actions/create-async-batch-jobs" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "urls[]": [
    "https://example.com"
  ]
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/scraperAPI/latest/actions/create-async-batch-jobs', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "urls[]": ["https://example.com"]
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `urls[]` | array<string> | yes | The list of target URLs to submit as async jobs. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "attempts": 1,
      "id": "string",
      "meta": {},
      "response": {},
      "status": "string",
      "statusUrl": "https://example.com",
      "supposedToRunAt": "2026-05-07T12:00:00.000Z",
      "url": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `attempts` | number |  |
| `id` | string |  |
| `meta` | object |  |
| `response` | object |  |
| `status` | string |  |
| `statusUrl` | string |  |
| `supposedToRunAt` | date |  |
| `url` | string |  |

## Native endpoint

Through the native ScraperAPI API, this operation is `POST https://async.scraperapi.com/batchjobs` (base URL `https://api.scraperapi.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-async-batch-jobs.md) for the provider-specific parameters and requirements.

