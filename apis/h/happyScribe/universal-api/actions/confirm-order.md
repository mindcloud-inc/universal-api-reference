# HappyScribe: Confirm Order

Confirms an order in HappyScribe.

```
PUT https://connect.mindcloud.co/v1/universal/happyScribe/latest/actions/confirm-order
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a HappyScribe `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/happyScribe/latest/actions/confirm-order" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "id": "49e1a97970944447b2dfe7ed5f00ce5a"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/happyScribe/latest/actions/confirm-order', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "id": "49e1a97970944447b2dfe7ed5f00ce5a"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `id` | string | yes | The order identifier. Default: `49e1a97970944447b2dfe7ed5f00ce5a`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "result": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `result` | string | HappyScribe returns an empty body on successful confirmation. |

## Native endpoint

Through the native HappyScribe API, this operation is `POST /orders/:id/confirm` (base URL `https://www.happyscribe.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/confirm-order.md) for the provider-specific parameters and requirements.

