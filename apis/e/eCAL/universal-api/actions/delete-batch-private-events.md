# ECAL: Delete Batch Private Events

Deletes batch private events from ECAL.

```
DELETE https://connect.mindcloud.co/v1/universal/eCAL/latest/actions/delete-batch-private-events
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ECAL `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/eCAL/latest/actions/delete-batch-private-events?connectionId=$CONNECTION_ID&requestBody=%5Bobject%20Object%5D" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "requestBody": "[object Object]"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/eCAL/latest/actions/delete-batch-private-events?${params}`, {
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
| `requestBody` | object | yes | JSON object matching ECAL's batch private event deletion body, for example {"ids":["event-id"]}. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "deletedIds": [
        "string"
      ],
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
| `deletedIds` | array<string> |  |
| `message` | string |  |
| `success` | boolean |  |

## Native endpoint

Through the native ECAL API, this operation is `DELETE /batch/events` (base URL `https://api.ecal.com/apiv2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-batch-private-events.md) for the provider-specific parameters and requirements.

