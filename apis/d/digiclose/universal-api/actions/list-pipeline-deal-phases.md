# Digiclose: List Pipeline Deal Phases



```
GET https://connect.mindcloud.co/v1/universal/digiclose/latest/actions/list-pipeline-deal-phases
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Digiclose `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/digiclose/latest/actions/list-pipeline-deal-phases?connectionId=$CONNECTION_ID&pipelineId=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "pipelineId": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/digiclose/latest/actions/list-pipeline-deal-phases?${params}`, {
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
| `pipelineId` | number | yes | Unique identifier for the pipeline. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "colorRgb": "string",
      "id": 1,
      "name": "Ava Chen"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `colorRgb` | string |  |
| `id` | number |  |
| `name` | string |  |

## Native endpoint

Through the native Digiclose API, this operation is `GET /pipelines/:pipeline_id/deal-phases` (base URL `https://app.digiclose.ai/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-pipeline-deal-phases.md) for the provider-specific parameters and requirements.

