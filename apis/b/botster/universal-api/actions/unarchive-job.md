# Botster: Unarchive Job

Unarchives an existing job in Botster.

```
PUT https://connect.mindcloud.co/v1/universal/botster/latest/actions/unarchive-job
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Botster `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/botster/latest/actions/unarchive-job" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "jobId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/botster/latest/actions/unarchive-job', {
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
      "job": {
        "bot": {
          "id": "string",
          "name": "Ava Chen"
        },
        "finished": true,
        "id": "string",
        "name": "Ava Chen",
        "state": "string"
      },
      "unarchived": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `job.bot.id` | string | Identifier of the Botster bot that owns the job. |
| `job.bot.name` | string | Display name of the Botster bot that owns the job. |
| `job.finished` | boolean | Whether the job has finished processing. |
| `job.id` | string | Unique Botster job identifier. |
| `job.name` | string | Botster job name. |
| `job.state` | string | Current Botster job state. |
| `unarchived` | boolean | Whether the unarchive request succeeded. |

## Native endpoint

Through the native Botster API, this operation is `POST /jobs/:jobId/unarchive` (base URL `https://botster.io/api/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/unarchive-job.md) for the provider-specific parameters and requirements.

