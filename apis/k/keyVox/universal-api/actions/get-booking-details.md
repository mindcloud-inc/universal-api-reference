# KeyVox: Get Booking Details

Retrieves booking details from your KeyVox account.

```
GET https://connect.mindcloud.co/v1/universal/keyVox/latest/actions/get-booking-details
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a KeyVox `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/keyVox/latest/actions/get-booking-details?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/keyVox/latest/actions/get-booking-details?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```



## Response

```json
{
  "success": true,
  "data": [
    {
      "orderId": "string",
      "orgId": "string",
      "placeId": "string",
      "placeName": "Ava Chen"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `orderId` | string | 注文番号 |
| `orgId` | string | 組織ID |
| `placeId` | string | 場所ID |
| `placeName` | string | 場所名 |

## Native endpoint

Through the native KeyVox API, this operation is `POST /bacsorder/detail` (base URL `https://eco.blockchainlock.io/api/eagle-pms`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-booking-details.md) for the provider-specific parameters and requirements.

