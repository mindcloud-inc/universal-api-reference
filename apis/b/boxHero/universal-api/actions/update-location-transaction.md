# BoxHero: Update Location Transaction



```
PUT https://connect.mindcloud.co/v1/universal/boxHero/latest/actions/update-location-transaction
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a BoxHero `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/boxHero/latest/actions/update-location-transaction" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "txId": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/boxHero/latest/actions/update-location-transaction', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "txId": 1
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `fromLocationId` | number | no | Source location ID |
| `items[]` | array<object> | no | Items included in the transaction |
| `memo` | string | no | Notes for the transaction |
| `partnerId` | number | no | Partner ID linked to the transaction |
| `revision` | number | no | Revision number for the transaction update |
| `toLocationId` | number | no | Destination location ID |
| `txId` | number | yes | Unique identifier for the transaction |

## Response

```json
{
  "success": true,
  "data": [
    {
      "id": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `id` | number |  |

## Native endpoint

Through the native BoxHero API, this operation is `PUT /v1/location-txs/:tx_id` (base URL `https://rest.boxhero-app.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-location-transaction.md) for the provider-specific parameters and requirements.

