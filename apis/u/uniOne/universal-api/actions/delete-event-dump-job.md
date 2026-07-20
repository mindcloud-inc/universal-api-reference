# UniOne: Delete Event Dump Job

Deletes an event dump job from UniOne.

```
DELETE https://connect.mindcloud.co/v1/universal/uniOne/latest/actions/delete-event-dump-job
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a UniOne `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/uniOne/latest/actions/delete-event-dump-job?connectionId=$CONNECTION_ID&dumpId=Gqfasjh34tlasd" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "dumpId": "Gqfasjh34tlasd"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/uniOne/latest/actions/delete-event-dump-job?${params}`, {
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
      "status": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `status` | string |  |

## Native endpoint

Through the native UniOne API, this operation is `POST event-dump/delete.json` (base URL `https://api.unione.io/en/transactional/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-event-dump-job.md) for the provider-specific parameters and requirements.

