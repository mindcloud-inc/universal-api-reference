# PostcardMania: Place Postcard Order

Creates a new postcard order in PostcardMania.

```
POST https://connect.mindcloud.co/v1/universal/postcardMania/latest/actions/place-postcard-order
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a PostcardMania `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/postcardMania/latest/actions/place-postcard-order" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/postcardMania/latest/actions/place-postcard-order', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `designID` | string | no | Existing approved design to use for the postcard order. |
| `front` | object | no | Front artwork object when not using designID. |
| `mailClass` | string | no | One of FirstClass or Standard. |
| `recipients[]` | array<object> | no | Recipient array. Validation requires 1 to 50000 items. |
| `size` | string | no | Required when designID is omitted. One of 46, 46S, 58, 68, 69, 611, 651. |
| `back` | object | no | Back design payload when designID is not supplied. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "orderID": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `orderID` | number | Created order identifier. |

## Native endpoint

Through the native PostcardMania API, this operation is `POST /order/postcard` (base URL `https://v3.pcmintegrations.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/place-postcard-order.md) for the provider-specific parameters and requirements.

