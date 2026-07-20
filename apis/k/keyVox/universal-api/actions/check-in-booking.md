# KeyVox: Check In Booking

Checks a booking in to KeyVox.

```
PUT https://connect.mindcloud.co/v1/universal/keyVox/latest/actions/check-in-booking
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a KeyVox `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/keyVox/latest/actions/check-in-booking" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/keyVox/latest/actions/check-in-booking', {
  method: 'PUT',
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



## Response

```json
{
  "success": true,
  "data": [
    {
      "value": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `value` | number | データ<br>レコード更新件数を返却します |

## Native endpoint

Through the native KeyVox API, this operation is `POST /bacsorder/checkin` (base URL `https://eco.blockchainlock.io/api/eagle-pms`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/check-in-booking.md) for the provider-specific parameters and requirements.

