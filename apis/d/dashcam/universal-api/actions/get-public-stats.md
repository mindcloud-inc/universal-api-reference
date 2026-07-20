# Dashcam: Get Public Stats

Retrieves public stats from Dashcam.

```
GET https://connect.mindcloud.co/v1/universal/dashcam/latest/actions/get-public-stats
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Dashcam `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/dashcam/latest/actions/get-public-stats?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/dashcam/latest/actions/get-public-stats?${params}`, {
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
      "executionTime": {},
      "repositories": 1,
      "successRate": 1,
      "testsPerDay": 1,
      "totalReplayDuration": 1,
      "totalReplayHours": 1,
      "totalTestsRun": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `executionTime` | object |  |
| `repositories` | number |  |
| `successRate` | number |  |
| `testsPerDay` | number |  |
| `totalReplayDuration` | number |  |
| `totalReplayHours` | number |  |
| `totalTestsRun` | number |  |

## Native endpoint

Through the native Dashcam API, this operation is `GET /api/v1/public/stats` (base URL `https://api.testdriver.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-public-stats.md) for the provider-specific parameters and requirements.

