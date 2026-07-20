# SingleStore: Save Schedule Settings

Updates schedule settings in SingleStore.

```
PUT https://connect.mindcloud.co/v1/universal/singleStore/latest/actions/save-schedule-settings
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a SingleStore `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/singleStore/latest/actions/save-schedule-settings" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "type": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/singleStore/latest/actions/save-schedule-settings', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "type": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `type` | string | yes | Scheduling mode to save for ingest runs. |
| `duration` | string | no | Schedule interval duration value. |
| `offset` | string | no | Offset to apply to the saved schedule. |
| `weekFlags` | string | no | Days of the week in YYYYYYY format, from Sunday through Saturday, when the schedule type is weekly. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native SingleStore API returns.

## Native endpoint

Through the native SingleStore API, this operation is `PATCH /config-sched` (base URL `https://{{credentials.flowEndpoint}}:30081/ingest/api/ingest`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/save-schedule-settings.md) for the provider-specific parameters and requirements.

