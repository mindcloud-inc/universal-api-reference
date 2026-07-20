# Late: Delete Queue Schedule



```
DELETE https://connect.mindcloud.co/v1/universal/late/latest/actions/delete-queue-schedule
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Late `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/late/latest/actions/delete-queue-schedule?connectionId=$CONNECTION_ID&profileId=string&queueId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "profileId": "string",
  "queueId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/late/latest/actions/delete-queue-schedule?${params}`, {
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
| `queueId` | string | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "deleted": true,
      "message": "string",
      "success": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `deleted` | boolean | Whether the queue was deleted. |
| `message` | string | Provider confirmation message. |
| `success` | boolean | Whether the delete request succeeded. |

## Native endpoint

Through the native Late API, this operation is `DELETE /queue/slots` (base URL `https://zernio.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-queue-schedule.md) for the provider-specific parameters and requirements.

