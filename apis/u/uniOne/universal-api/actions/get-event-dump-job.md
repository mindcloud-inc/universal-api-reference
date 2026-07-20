# UniOne: Get Event Dump Job

Retrieves an event dump job from UniOne.

```
GET https://connect.mindcloud.co/v1/universal/uniOne/latest/actions/get-event-dump-job
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a UniOne `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/uniOne/latest/actions/get-event-dump-job?connectionId=$CONNECTION_ID&dumpId=Gqfasjh34tlasd" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "dumpId": "Gqfasjh34tlasd"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/uniOne/latest/actions/get-event-dump-job?${params}`, {
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
| `dumpId` | string | yes | Dump identifier returned by Create Event Dump Job. Example: `Gqfasjh34tlasd`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "event_dump": {
        "dump_id": "string",
        "dump_status": "string",
        "files": [
          {}
        ]
      },
      "status": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `event_dump.dump_id` | string |  |
| `event_dump.dump_status` | string |  |
| `event_dump.files` | array<object> |  |
| `status` | string |  |

## Native endpoint

Through the native UniOne API, this operation is `POST event-dump/get.json` (base URL `https://api.unione.io/en/transactional/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-event-dump-job.md) for the provider-specific parameters and requirements.

