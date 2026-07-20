# Port API AI: Approve Action Run

Approves an action run in Port.

```
PUT https://connect.mindcloud.co/v1/universal/portAPIAI/latest/actions/approve-action-run
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Port API AI `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/portAPIAI/latest/actions/approve-action-run" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "runId": "string",
  "status": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/portAPIAI/latest/actions/approve-action-run', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "runId": "string",
    "status": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `runId` | string | yes | The Port action run identifier. |
| `status` | string | yes | Approval decision |

## Response

```json
{
  "success": true,
  "data": [
    {
      "ok": true,
      "run": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `ok` | boolean |  |
| `run` | object |  |

## Native endpoint

Through the native Port API AI API, this operation is `PATCH /actions/runs/:run_id/approval` (base URL `https://api.port.io/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/approve-action-run.md) for the provider-specific parameters and requirements.

