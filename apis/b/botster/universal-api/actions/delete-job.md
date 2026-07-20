# Botster: Delete Job

Deletes an existing job from Botster.

```
DELETE https://connect.mindcloud.co/v1/universal/botster/latest/actions/delete-job
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Botster `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/botster/latest/actions/delete-job?connectionId=$CONNECTION_ID&jobId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "jobId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/botster/latest/actions/delete-job?${params}`, {
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
| `jobId` | string | yes | The Botster job UUID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "deleted": true,
      "job": {
        "bot": {
          "id": "string",
          "name": "Ava Chen"
        },
        "finished": true,
        "id": "string",
        "name": "Ava Chen",
        "state": "string"
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `deleted` | boolean | Whether the delete request succeeded. |
| `job.bot.id` | string | Identifier of the Botster bot that owned the job. |
| `job.bot.name` | string | Display name of the Botster bot that owned the job. |
| `job.finished` | boolean | Whether the job had finished processing before deletion. |
| `job.id` | string | Unique Botster job identifier. |
| `job.name` | string | Botster job name. |
| `job.state` | string | Current Botster job state at deletion time. |

## Native endpoint

Through the native Botster API, this operation is `DELETE /jobs/:jobId` (base URL `https://botster.io/api/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-job.md) for the provider-specific parameters and requirements.

