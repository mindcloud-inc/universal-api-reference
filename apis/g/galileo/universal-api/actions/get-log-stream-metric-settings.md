# Galileo: Get Log Stream Metric Settings

Retrieves metric settings for a Galileo log stream.

```
GET https://connect.mindcloud.co/v1/universal/galileo/latest/actions/get-log-stream-metric-settings
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Galileo `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/galileo/latest/actions/get-log-stream-metric-settings?connectionId=$CONNECTION_ID&logStreamId=string&projectId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "logStreamId": "string",
  "projectId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/galileo/latest/actions/get-log-stream-metric-settings?${params}`, {
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
| `logStreamId` | string | yes | Galileo log stream UUID. |
| `projectId` | string | yes | Galileo project UUID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "scorers": [
        {
          "cotEnabled": true,
          "filters": [
            {
              "caseSensitive": true,
              "name": "Ava Chen",
              "operator": "string",
              "value": "string"
            }
          ],
          "id": "string",
          "inputType": "string",
          "modelName": "Ava Chen",
          "modelType": "string",
          "multimodalCapabilities": [
            "string"
          ],
          "name": "Ava Chen",
          "numJudges": 1,
          "outputType": "string",
          "rollUpMethod": "string",
          "scoreableNodeTypes": [
            "string"
          ],
          "scorerType": "string",
          "scorerVersion": {},
          "scoreType": "string"
        }
      ],
      "segmentFilters": [
        {
          "filter": {},
          "llmScorers": true,
          "sampleRate": 1
        }
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `scorers` | array<object> |  |
| `scorers[].cotEnabled` | boolean |  |
| `scorers[].filters` | array<object> |  |
| `scorers[].filters[].caseSensitive` | boolean |  |
| `scorers[].filters[].name` | string |  |
| `scorers[].filters[].operator` | string |  |
| `scorers[].filters[].value` | string |  |
| `scorers[].id` | string |  |
| `scorers[].inputType` | string |  |
| `scorers[].modelName` | string |  |
| `scorers[].modelType` | string |  |
| `scorers[].multimodalCapabilities` | array<string> |  |
| `scorers[].name` | string |  |
| `scorers[].numJudges` | number |  |
| `scorers[].outputType` | string |  |
| `scorers[].rollUpMethod` | string |  |
| `scorers[].scoreableNodeTypes` | array<string> |  |
| `scorers[].scorerType` | string |  |
| `scorers[].scorerVersion` | object |  |
| `scorers[].scoreType` | string |  |
| `segmentFilters` | array<object> |  |
| `segmentFilters[].filter` | object |  |
| `segmentFilters[].llmScorers` | boolean |  |
| `segmentFilters[].sampleRate` | number |  |

## Native endpoint

Through the native Galileo API, this operation is `GET /v2/projects/:project_id/log_streams/:log_stream_id/metric_settings` (base URL `https://api.galileo.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-log-stream-metric-settings.md) for the provider-specific parameters and requirements.

