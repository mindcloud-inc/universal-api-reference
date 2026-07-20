# Better Stack Telemetry: Remove Exploration Alert

Deletes an existing exploration alert from Better Stack Telemetry.

```
DELETE https://connect.mindcloud.co/v1/universal/betterStackTelemetry/latest/actions/remove-exploration-alert
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Better Stack Telemetry `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/betterStackTelemetry/latest/actions/remove-exploration-alert?connectionId=$CONNECTION_ID&explorationId=746510&id=1857617807" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "explorationId": "746510",
  "id": "1857617807"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/betterStackTelemetry/latest/actions/remove-exploration-alert?${params}`, {
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
| `explorationId` | string | yes | The ID of the exploration that owns the alert. Example: `746510`. |
| `id` | string | yes | The ID of the alert to remove. Example: `1857617807`. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Better Stack Telemetry API returns.

## Native endpoint

Through the native Better Stack Telemetry API, this operation is `DELETE /api/v2/explorations/:exploration_id/alerts/:id` (base URL `https://telemetry.betterstack.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/remove-exploration-alert.md) for the provider-specific parameters and requirements.

