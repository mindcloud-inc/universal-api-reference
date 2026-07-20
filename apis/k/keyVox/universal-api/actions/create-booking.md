# KeyVox: Create Booking

Creates a new booking in KeyVox.

```
POST https://connect.mindcloud.co/v1/universal/keyVox/latest/actions/create-booking
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a KeyVox `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/keyVox/latest/actions/create-booking" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/keyVox/latest/actions/create-booking', {
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
| `channelOrderNo` | string | no | 予約サイト予約番号 |
| `checkin` | string | no | チェックイン時間<br>UNIX時間（秒）で指定します |
| `checkout` | string | no | チェックアウト時間<br>UNIX時間（秒）で指定します |
| `contactAddress` | string | no | お客様住所 |
| `contactCertificateNum` | string | no | お客様証明書ID |
| `orderContact` | string | no | お客様氏名 |
| `orderSource` | string | no | 予約サイト名(システム名) |
| `placeId` | string | no | 場所ID |
| `userId` | string | no | ユーザーID |

## Response

```json
{
  "success": true,
  "data": [
    {
      "orderId": "string",
      "orderSource": "string",
      "orgId": "string",
      "placeId": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `orderId` | string | 注文番号 |
| `orderSource` | string | 予約サイト名(システム名) |
| `orgId` | string | 組織ID |
| `placeId` | string | 場所ID |

## Native endpoint

Through the native KeyVox API, this operation is `POST /bacsorder/create` (base URL `https://eco.blockchainlock.io/api/eagle-pms`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-booking.md) for the provider-specific parameters and requirements.

