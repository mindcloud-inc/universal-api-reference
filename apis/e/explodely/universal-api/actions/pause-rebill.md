# Explodely: Pause Rebill

Updates a rebill in Explodely by delaying the next charge.

```
PUT https://connect.mindcloud.co/v1/universal/explodely/latest/actions/pause-rebill
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Explodely `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/explodely/latest/actions/pause-rebill" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "mainOrderId": "236084113",
  "delayDays": "7"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/explodely/latest/actions/pause-rebill', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "mainOrderId": "236084113",
    "delayDays": "7"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `mainOrderId` | string | yes | The initial Explodely order ID for the rebill sale. Example: `236084113`. |
| `delayDays` | string | yes | The number of days to delay the next rebill, up to 30. Example: `7`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "error": "string",
      "mainorderid": "string",
      "rebillcancel": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `error` | string |  |
| `mainorderid` | string |  |
| `rebillcancel` | string |  |

## Native endpoint

Through the native Explodely API, this operation is `GET /rebill` (base URL `https://explodely.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/pause-rebill.md) for the provider-specific parameters and requirements.

