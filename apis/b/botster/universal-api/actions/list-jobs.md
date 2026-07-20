# Botster: List Jobs

Retrieves the jobs in your Botster account.

```
GET https://connect.mindcloud.co/v1/universal/botster/latest/actions/list-jobs
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Botster `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/botster/latest/actions/list-jobs?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/botster/latest/actions/list-jobs?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```



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
      "finished": true,
      "id": "string",
      "name": "Ava Chen",
      "state": "string"
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
| `finished` | boolean | Whether the job has finished processing. |
| `id` | string | Unique Botster job identifier. |
| `name` | string | Botster job name. |
| `state` | string | Current Botster job state. |

## Native endpoint

Through the native Botster API, this operation is `GET /jobs` (base URL `https://botster.io/api/v2`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-jobs.md) for the provider-specific parameters and requirements.

