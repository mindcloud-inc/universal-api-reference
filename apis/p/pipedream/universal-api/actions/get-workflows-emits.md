# Pipedream: Get workflow emits

Retrieves emitted event summaries for a workflow in Pipedream.

```
GET https://connect.mindcloud.co/v1/universal/pipedream/latest/actions/get-workflows-emits
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Pipedream `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/pipedream/latest/actions/get-workflows-emits?connectionId=$CONNECTION_ID&workflowId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "workflowId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/pipedream/latest/actions/get-workflows-emits?${params}`, {
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
| `workflowId` | string | yes | The workflow identifier. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "event": {},
      "id": "string",
      "indexedAtMs": 1,
      "metadata": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `event` | object |  |
| `id` | string |  |
| `indexedAtMs` | number |  |
| `metadata` | object |  |

## Native endpoint

Through the native Pipedream API, this operation is `GET /workflows/{workflow_id}/event_summaries` (base URL `https://api.pipedream.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-workflows-emits.md) for the provider-specific parameters and requirements.

