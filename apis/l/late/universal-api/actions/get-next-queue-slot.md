# Late: Get Next Queue Slot



```
GET https://connect.mindcloud.co/v1/universal/late/latest/actions/get-next-queue-slot
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Late `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/late/latest/actions/get-next-queue-slot?connectionId=$CONNECTION_ID&profileId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "profileId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/late/latest/actions/get-next-queue-slot?${params}`, {
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
| `profileId` | string | yes |  |
| `queueId` | string | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "nextSlot": "2026-05-07T12:00:00.000Z",
      "profileId": "string",
      "queueId": "string",
      "queueName": "Ava Chen",
      "timezone": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `nextSlot` | date | Next queue slot timestamp. |
| `profileId` | string | Profile identifier. |
| `queueId` | string | Queue identifier. |
| `queueName` | string | Queue name. |
| `timezone` | string | Timezone used for the queue. |

## Native endpoint

Through the native Late API, this operation is `GET /queue/next-slot` (base URL `https://zernio.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-next-queue-slot.md) for the provider-specific parameters and requirements.

