# CustomGPT.ai: Get Agent Statistics

Retrieves detailed agent statistics from CustomGPT.ai.

```
GET https://connect.mindcloud.co/v1/universal/customGPTai/latest/actions/get-agent-statistics
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a CustomGPT.ai `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/customGPTai/latest/actions/get-agent-statistics?connectionId=$CONNECTION_ID&projectId=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "projectId": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/customGPTai/latest/actions/get-agent-statistics?${params}`, {
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
| `projectId` | number | yes | The project ID of the agent to inspect. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "crawlCreditsUsed": 1,
      "pagesCrawled": 1,
      "pagesFound": 1,
      "pagesIndexed": 1,
      "queryCreditsUsed": 1,
      "totalQueries": 1,
      "totalStorageCreditsUsed": 1,
      "totalWordsIndexed": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `crawlCreditsUsed` | number |  |
| `pagesCrawled` | number |  |
| `pagesFound` | number |  |
| `pagesIndexed` | number |  |
| `queryCreditsUsed` | number |  |
| `totalQueries` | number |  |
| `totalStorageCreditsUsed` | number |  |
| `totalWordsIndexed` | number |  |

## Native endpoint

Through the native CustomGPT.ai API, this operation is `GET /projects/:projectId/stats` (base URL `https://app.customgpt.ai/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-agent-statistics.md) for the provider-specific parameters and requirements.

