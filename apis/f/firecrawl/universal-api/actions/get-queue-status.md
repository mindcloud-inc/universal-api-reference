# Firecrawl: Get Queue Status

Retrieves queue status from Firecrawl.

```
GET https://connect.mindcloud.co/v1/universal/firecrawl/latest/actions/get-queue-status
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Firecrawl `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/firecrawl/latest/actions/get-queue-status?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/firecrawl/latest/actions/get-queue-status?${params}`, {
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
      "activeJobsInQueue": 1,
      "jobsInQueue": 1,
      "maxConcurrency": 1,
      "mostRecentSuccess": "2026-05-07T12:00:00.000Z",
      "waitingJobsInQueue": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `activeJobsInQueue` | number |  |
| `jobsInQueue` | number |  |
| `maxConcurrency` | number |  |
| `mostRecentSuccess` | date |  |
| `waitingJobsInQueue` | number |  |

## Native endpoint

Through the native Firecrawl API, this operation is `GET /team/queue-status` (base URL `https://api.firecrawl.dev/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-queue-status.md) for the provider-specific parameters and requirements.

