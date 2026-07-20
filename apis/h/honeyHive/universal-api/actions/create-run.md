# HoneyHive: Create Run

Creates a new evaluation run in HoneyHive.

```
POST https://connect.mindcloud.co/v1/universal/honeyHive/latest/actions/create-run
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a HoneyHive `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/honeyHive/latest/actions/create-run" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "project": "string",
  "name": "Ava Chen",
  "eventIds[]": [
    "string"
  ]
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/honeyHive/latest/actions/create-run', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "project": "string",
    "name": "Ava Chen",
    "eventIds[]": ["string"]
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `project` | string | yes | Project name. |
| `name` | string | yes | Run name. |
| `eventIds[]` | array<string> | yes | Event IDs for the run. |

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
      },
      "runId": "string"
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
| `runId` | string |  |

## Native endpoint

Through the native HoneyHive API, this operation is `POST /runs` (base URL `https://api.honeyhive.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-run.md) for the provider-specific parameters and requirements.

