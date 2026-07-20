# PushAlert: Add Subscribers To Segment



```
PUT https://connect.mindcloud.co/v1/universal/pushAlert/latest/actions/add-subscribers-to-segment
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a PushAlert `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/pushAlert/latest/actions/add-subscribers-to-segment" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "segId": "string",
  "subscribers": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/pushAlert/latest/actions/add-subscribers-to-segment', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "segId": "string",
    "subscribers": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `segId` | string | yes | PushAlert segment ID. |
| `subscribers` | string | yes | JSON array string of subscriber IDs to add to the segment. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "msg": "string",
      "success": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `msg` | string | Provider message returned for the segment add request. |
| `success` | boolean | Whether adding subscribers to the segment succeeded. |

## Native endpoint

Through the native PushAlert API, this operation is `POST /rest/v2/web-push/segment/:segId/add` (base URL `https://api.pushalert.co`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/add-subscribers-to-segment.md) for the provider-specific parameters and requirements.

