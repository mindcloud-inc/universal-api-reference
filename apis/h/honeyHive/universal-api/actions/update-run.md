# HoneyHive: Update Run

Updates an evaluation run in HoneyHive.

```
PUT https://connect.mindcloud.co/v1/universal/honeyHive/latest/actions/update-run
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a HoneyHive `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/honeyHive/latest/actions/update-run" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "runId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/honeyHive/latest/actions/update-run', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "runId": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `runId` | string | yes | Run ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "evaluation": {},
      "warning": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `evaluation` | object |  |
| `warning` | string |  |

## Native endpoint

Through the native HoneyHive API, this operation is `PUT /runs/{run_id}` (base URL `https://api.honeyhive.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-run.md) for the provider-specific parameters and requirements.

