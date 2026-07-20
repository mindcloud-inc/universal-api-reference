# Digiclose: Get Pipeline



```
GET https://connect.mindcloud.co/v1/universal/digiclose/latest/actions/get-pipeline
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Digiclose `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/digiclose/latest/actions/get-pipeline?connectionId=$CONNECTION_ID&pipelineId=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "pipelineId": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/digiclose/latest/actions/get-pipeline?${params}`, {
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
      "dealPhases": [
        {
          "colorRgb": "string",
          "id": 1,
          "name": "Ava Chen"
        }
      ],
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
| `dealPhases[].colorRgb` | string |  |
| `dealPhases[].id` | number |  |
| `dealPhases[].name` | string |  |
| `id` | number |  |
| `name` | string |  |

## Native endpoint

Through the native Digiclose API, this operation is `GET /pipelines/:pipeline_id` (base URL `https://app.digiclose.ai/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-pipeline.md) for the provider-specific parameters and requirements.

