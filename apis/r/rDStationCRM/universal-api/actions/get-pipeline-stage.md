# RD Station CRM: Get Pipeline Stage

Retrieves a sales pipeline stage from RD Station CRM.

```
GET https://connect.mindcloud.co/v1/universal/rDStationCRM/latest/actions/get-pipeline-stage
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a RD Station CRM `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/rDStationCRM/latest/actions/get-pipeline-stage?connectionId=$CONNECTION_ID&id=string&pipelineId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "string",
  "pipelineId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/rDStationCRM/latest/actions/get-pipeline-stage?${params}`, {
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
| `id` | string | yes | Stage identifier. |
| `pipelineId` | string | yes | Pipeline identifier. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "data": {
        "createdAt": "string",
        "id": "string",
        "name": "Ava Chen",
        "order": 1,
        "updatedAt": "string"
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data` | object |  |
| `data.createdAt` | string |  |
| `data.id` | string |  |
| `data.name` | string |  |
| `data.order` | number |  |
| `data.updatedAt` | string |  |

## Native endpoint

Through the native RD Station CRM API, this operation is `GET /pipelines/:pipeline_id/stages/:id` (base URL `https://api.rd.services/crm/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-pipeline-stage.md) for the provider-specific parameters and requirements.

