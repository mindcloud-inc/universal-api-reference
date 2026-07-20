# Botster: Restart Job

Restarts an existing job in Botster.

```
PUT https://connect.mindcloud.co/v1/universal/botster/latest/actions/restart-job
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Botster `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/botster/latest/actions/restart-job" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "jobId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/botster/latest/actions/restart-job', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "jobId": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `jobId` | string | yes | The Botster job UUID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "bot": {
        "id": "string",
        "name": "Ava Chen"
      },
      "created_at": 1,
      "id": "string",
      "name": "Ava Chen",
      "success": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `bot.id` | string | Identifier of the Botster bot that owns the job. |
| `bot.name` | string | Display name of the Botster bot that owns the job. |
| `created_at` | number | Unix timestamp when the job was created. |
| `id` | string | Unique Botster job identifier. |
| `name` | string | Botster job name. |
| `success` | boolean | Whether the restart request succeeded. |

## Native endpoint

Through the native Botster API, this operation is `POST /jobs/:jobId/restart` (base URL `https://botster.io/api/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/restart-job.md) for the provider-specific parameters and requirements.

