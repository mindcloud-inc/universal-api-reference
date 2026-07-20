# Onfleet: List Worker Tasks

Retrieves tasks assigned to a worker in Onfleet.

```
GET https://connect.mindcloud.co/v1/universal/onfleet/latest/actions/list-worker-tasks
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Onfleet `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/onfleet/latest/actions/list-worker-tasks?connectionId=$CONNECTION_ID&workerId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "workerId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/onfleet/latest/actions/list-worker-tasks?${params}`, {
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
| `workerId` | string | yes | The Onfleet worker ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "tasks": [
        "string"
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `tasks` | array |  |

## Native endpoint

Through the native Onfleet API, this operation is `GET /workers/:workerId/tasks` (base URL `https://onfleet.com/api/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-worker-tasks.md) for the provider-specific parameters and requirements.

