# Middesk: Retrieve an agent run

Retrieves an agent run from Middesk.

```
GET https://connect.mindcloud.co/v1/universal/middesk/latest/actions/get-agent-run
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Middesk `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/middesk/latest/actions/get-agent-run?connectionId=$CONNECTION_ID&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/middesk/latest/actions/get-agent-run?${params}`, {
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
| `id` | string | yes | ID of the agent run to retrieve. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "createdAt": "string",
      "endedAt": "string",
      "id": "string",
      "interrupts": [
        {}
      ],
      "object": "string",
      "startedAt": "string",
      "status": "string",
      "steps": [
        {}
      ],
      "updatedAt": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `createdAt` | string |  |
| `endedAt` | string |  |
| `id` | string |  |
| `interrupts` | array<object> |  |
| `object` | string |  |
| `startedAt` | string |  |
| `status` | string |  |
| `steps` | array<object> |  |
| `updatedAt` | string |  |

## Native endpoint

Through the native Middesk API, this operation is `GET /runs/:id` (base URL `https://api.middesk.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-agent-run.md) for the provider-specific parameters and requirements.

