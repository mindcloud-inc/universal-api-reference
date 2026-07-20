# OkoCRM: List pipeline stages

Retrieves pipeline stages for a pipeline in OkoCRM.

```
GET https://connect.mindcloud.co/v1/universal/okoCRM/latest/actions/list-pipeline-stages
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a OkoCRM `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/okoCRM/latest/actions/list-pipeline-stages?connectionId=$CONNECTION_ID&pipeline_id=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "pipeline_id": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/okoCRM/latest/actions/list-pipeline-stages?${params}`, {
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
| `pipeline_id` | number | yes | The OkoCRM pipeline ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "color": "string",
      "id": 1,
      "name": "Ava Chen",
      "pipeline_id": 1,
      "sort": 1,
      "system": 1,
      "type": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `color` | string |  |
| `id` | number |  |
| `name` | string |  |
| `pipeline_id` | number |  |
| `sort` | number |  |
| `system` | number |  |
| `type` | string |  |

## Native endpoint

Through the native OkoCRM API, this operation is `GET /pipelines/stages/[:pipeline_id]` (base URL `https://api.okocrm.com/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-pipeline-stages.md) for the provider-specific parameters and requirements.

