# Pinghome: Update Statuspage Status

Updates statuspage status in Pinghome.

```
PUT https://connect.mindcloud.co/v1/universal/pinghome/latest/actions/update-statuspage-status
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Pinghome `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/pinghome/latest/actions/update-statuspage-status" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "statuspageId": "string",
  "enabled": true
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/pinghome/latest/actions/update-statuspage-status', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "statuspageId": "string",
    "enabled": true
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `statuspageId` | string | yes | The unique ID of the statuspage. |
| `enabled` | boolean | yes | Whether the statuspage should be enabled. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Pinghome API returns.

## Native endpoint

Through the native Pinghome API, this operation is `PUT /statuspage-cmd/v1/statuspage/:id/status` (base URL `https://api.pinghome.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-statuspage-status.md) for the provider-specific parameters and requirements.

