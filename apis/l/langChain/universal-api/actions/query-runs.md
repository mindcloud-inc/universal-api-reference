# LangChain: Query Runs



```
GET https://connect.mindcloud.co/v1/universal/langChain/latest/actions/query-runs
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a LangChain `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/langChain/latest/actions/query-runs?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/langChain/latest/actions/query-runs?${params}`, {
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
      "cursors": {
        "next": {},
        "prev": {}
      },
      "parsedQuery": {},
      "runs": [
        {
          "appPath": "string",
          "childRunIds": {},
          "completionCost": {},
          "completionCostDetails": {},
          "completionTokenDetails": {},
          "completionTokens": 1,
          "directChildRunIds": {},
          "dottedOrder": "string",
          "endTime": {},
          "error": {},
          "executionOrder": 1,
          "extra": {
            "metadata": {
              "lsRunDepth": 1
            }
          },
          "feedbackStats": {},
          "firstTokenTime": {},
          "id": "string",
          "inDataset": true,
          "inputs": {
            "prompt": "string"
          },
          "inputsPreview": {},
          "inputsS3Urls": {},
          "lastQueuedAt": {},
          "manifestId": {},
          "manifestS3Id": {},
          "messages": {},
          "name": "Ava Chen",
          "outputs": {},
          "outputsPreview": {},
          "outputsS3Urls": {},
          "parentRunId": {},
          "priceModelId": {},
          "promptCost": {},
          "promptCostDetails": {},
          "promptTokenDetails": {},
          "promptTokens": 1,
          "referenceDatasetId": {},
          "referenceExampleId": {},
          "runType": "string",
          "s3Urls": {},
          "serialized": {},
          "sessionId": "string",
          "shareToken": {},
          "startTime": "string",
          "status": "string",
          "threadId": {},
          "totalCost": {},
          "totalTokens": 1,
          "traceFirstReceivedAt": "string",
          "traceId": "string",
          "traceMaxStartTime": {},
          "traceMinStartTime": {},
          "traceTier": "string",
          "traceUpgrade": true,
          "ttlSeconds": 1
        }
      ],
      "searchCursors": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `cursors.next` | object |  |
| `cursors.prev` | object |  |
| `parsedQuery` | object |  |
| `runs[].appPath` | string |  |
| `runs[].childRunIds` | object |  |
| `runs[].completionCost` | object |  |
| `runs[].completionCostDetails` | object |  |
| `runs[].completionTokenDetails` | object |  |
| `runs[].completionTokens` | number |  |
| `runs[].directChildRunIds` | object |  |
| `runs[].dottedOrder` | string |  |
| `runs[].endTime` | object |  |
| `runs[].error` | object |  |
| `runs[].executionOrder` | number |  |
| `runs[].extra.metadata.lsRunDepth` | number |  |
| `runs[].feedbackStats` | object |  |
| `runs[].firstTokenTime` | object |  |
| `runs[].id` | string |  |
| `runs[].inDataset` | boolean |  |
| `runs[].inputs.prompt` | string |  |
| `runs[].inputsPreview` | object |  |
| `runs[].inputsS3Urls` | object |  |
| `runs[].lastQueuedAt` | object |  |
| `runs[].manifestId` | object |  |
| `runs[].manifestS3Id` | object |  |
| `runs[].messages` | object |  |
| `runs[].name` | string |  |
| `runs[].outputs` | object |  |
| `runs[].outputsPreview` | object |  |
| `runs[].outputsS3Urls` | object |  |
| `runs[].parentRunId` | object |  |
| `runs[].priceModelId` | object |  |
| `runs[].promptCost` | object |  |
| `runs[].promptCostDetails` | object |  |
| `runs[].promptTokenDetails` | object |  |
| `runs[].promptTokens` | number |  |
| `runs[].referenceDatasetId` | object |  |
| `runs[].referenceExampleId` | object |  |
| `runs[].runType` | string |  |
| `runs[].s3Urls` | object |  |
| `runs[].serialized` | object |  |
| `runs[].sessionId` | string |  |
| `runs[].shareToken` | object |  |
| `runs[].startTime` | string |  |
| `runs[].status` | string |  |
| `runs[].threadId` | object |  |
| `runs[].totalCost` | object |  |
| `runs[].totalTokens` | number |  |
| `runs[].traceFirstReceivedAt` | string |  |
| `runs[].traceId` | string |  |
| `runs[].traceMaxStartTime` | object |  |
| `runs[].traceMinStartTime` | object |  |
| `runs[].traceTier` | string |  |
| `runs[].traceUpgrade` | boolean |  |
| `runs[].ttlSeconds` | number |  |
| `searchCursors` | object |  |

## Native endpoint

Through the native LangChain API, this operation is `POST /api/v1/runs/query` (base URL `https://api.smith.langchain.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/query-runs.md) for the provider-specific parameters and requirements.

