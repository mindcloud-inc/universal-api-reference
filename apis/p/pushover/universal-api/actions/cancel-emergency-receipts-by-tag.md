# Pushover: Cancel Emergency Receipts by Tag



```
PUT https://connect.mindcloud.co/v1/universal/pushover/latest/actions/cancel-emergency-receipts-by-tag
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Pushover `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/pushover/latest/actions/cancel-emergency-receipts-by-tag" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "tag": "l=chicago"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/pushover/latest/actions/cancel-emergency-receipts-by-tag', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "tag": "l=chicago"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `tag` | string | yes | Tag used to cancel active emergency-priority messages. Example: `l=chicago`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "canceled": 1,
      "request": "string",
      "status": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `canceled` | number | Count of active emergency-priority receipts canceled for the tag. |
| `request` | string | Pushover request identifier. |
| `status` | number | API status. Returns 1 when the cancel-by-tag request succeeds. |

## Native endpoint

Through the native Pushover API, this operation is `POST /receipts/cancel_by_tag/:tag.json` (base URL `https://api.pushover.net/1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/cancel-emergency-receipts-by-tag.md) for the provider-specific parameters and requirements.

