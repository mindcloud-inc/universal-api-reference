# HoneyHive: Get Run

Retrieves an evaluation run from HoneyHive.

```
GET https://connect.mindcloud.co/v1/universal/honeyHive/latest/actions/get-run
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a HoneyHive `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/honeyHive/latest/actions/get-run?connectionId=$CONNECTION_ID&runId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "runId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/honeyHive/latest/actions/get-run?${params}`, {
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
| `runId` | string | yes | Run ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "evaluation": {
        "configuration": {},
        "createdAt": "string",
        "datapointIds": [
          "string"
        ],
        "datasetId": "string",
        "eventIds": [
          "string"
        ],
        "metadata": {},
        "name": "Ava Chen",
        "project": "string",
        "results": {},
        "runId": "string",
        "status": "string"
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `evaluation` | object |  |
| `evaluation.configuration` | object |  |
| `evaluation.createdAt` | string |  |
| `evaluation.datapointIds` | array<string> |  |
| `evaluation.datasetId` | string |  |
| `evaluation.eventIds` | array<string> |  |
| `evaluation.metadata` | object |  |
| `evaluation.name` | string |  |
| `evaluation.project` | string |  |
| `evaluation.results` | object |  |
| `evaluation.runId` | string |  |
| `evaluation.status` | string |  |

## Native endpoint

Through the native HoneyHive API, this operation is `GET /runs/{run_id}` (base URL `https://api.honeyhive.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-run.md) for the provider-specific parameters and requirements.

