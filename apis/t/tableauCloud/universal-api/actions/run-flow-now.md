# Tableau Cloud: Run Flow Now

Runs a flow in Tableau Cloud.

```
POST https://connect.mindcloud.co/v1/universal/tableauCloud/latest/actions/run-flow-now
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Tableau Cloud `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/tableauCloud/latest/actions/run-flow-now" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/tableauCloud/latest/actions/run-flow-now', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId
  })
});

const { success, data } = await response.json();
```



## Response

```json
{
  "success": true,
  "data": [
    {
      "createdAt": "string",
      "id": "string",
      "mode": "string",
      "runFlowJobType": {
        "flow": {
          "id": "string",
          "name": "Ava Chen"
        },
        "flowRunId": "string"
      },
      "type": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `createdAt` | string | Job creation timestamp. |
| `id` | string | Job ID. |
| `mode` | string | Job execution mode. |
| `runFlowJobType.flow.id` | string | Flow ID. |
| `runFlowJobType.flow.name` | string | Flow name. |
| `runFlowJobType.flowRunId` | string | Flow run ID. |
| `type` | string | Job type. |

## Native endpoint

Through the native Tableau Cloud API, this operation is `POST /sites/site-id/flows/flow-id/run` (base URL `https://us-east-1.online.tableau.com/api/3.28`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/run-flow-now.md) for the provider-specific parameters and requirements.

