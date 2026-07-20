# Hightouch: Get Decision Engine Flow

Retrieves a decision engine flow from Hightouch.

```
GET https://connect.mindcloud.co/v1/universal/hightouch/latest/actions/get-decision-engine-flow
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Hightouch `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/hightouch/latest/actions/get-decision-engine-flow?connectionId=$CONNECTION_ID&flowId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "flowId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/hightouch/latest/actions/get-decision-engine-flow?${params}`, {
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
| `flowId` | string | yes | The Decision Engine flow ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "audienceId": 1,
      "config": {},
      "createdAt": "2026-05-07T12:00:00.000Z",
      "decisionEngineId": "string",
      "id": "string",
      "name": "Ava Chen",
      "status": "string",
      "updatedAt": "2026-05-07T12:00:00.000Z",
      "workspaceId": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `audienceId` | number | Audience ID. |
| `config` | object | Flow configuration. |
| `createdAt` | date | Creation timestamp. |
| `decisionEngineId` | string | Decision engine ID. |
| `id` | string | Decision engine flow ID. |
| `name` | string | Decision engine flow name. |
| `status` | string | Flow status. |
| `updatedAt` | date | Last update timestamp. |
| `workspaceId` | number | Workspace ID. |

## Native endpoint

Through the native Hightouch API, this operation is `GET /decision-engine/flow/{flowId}` (base URL `https://api.hightouch.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-decision-engine-flow.md) for the provider-specific parameters and requirements.

