# Valyu: Update DeepResearch Task



```
PUT https://connect.mindcloud.co/v1/universal/valyu/latest/actions/update-deep-research-task
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Valyu `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/valyu/latest/actions/update-deep-research-task" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "id": "string",
  "instruction": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/valyu/latest/actions/update-deep-research-task', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "id": "string",
    "instruction": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `id` | string | yes | The DeepResearch task ID. |
| `instruction` | string | yes | Follow-up instruction for the research agent. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "deepresearchId": "string",
      "message": "string",
      "success": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `deepresearchId` | string |  |
| `message` | string |  |
| `success` | boolean |  |

## Native endpoint

Through the native Valyu API, this operation is `POST /deepresearch/tasks/:id/update` (base URL `https://api.valyu.ai/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-deep-research-task.md) for the provider-specific parameters and requirements.

