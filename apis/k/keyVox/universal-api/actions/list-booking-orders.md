# KeyVox: List Booking Orders

Lists booking orders in your KeyVox account.

```
GET https://connect.mindcloud.co/v1/universal/keyVox/latest/actions/list-booking-orders
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a KeyVox `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/keyVox/latest/actions/list-booking-orders?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/keyVox/latest/actions/list-booking-orders?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as query string parameters ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `unitId` | string | no | WEB管理画面「BACS」で設定したドア(部屋)ごとに割り当てられるユニークIDです。getUnitsで取得可能です |

## Response

```json
{
  "success": true,
  "data": [
    {
      "checkIn": "string",
      "checkOut": "string",
      "orderId": "string",
      "pinCode": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `checkIn` | string | チェックイン予定日時、1970/01/01からの秒数(UNIX時間)で指定します |
| `checkOut` | string | チェックアウト予定日時、1970/01/01からの秒数(UNIX時間)で指定します |
| `orderId` | string | 予約番号 |
| `pinCode` | string | スマートロックに配信される6桁の暗証番号です |

## Native endpoint

Through the native KeyVox API, this operation is `POST /v1/getBookingOrders` (base URL `https://eco.blockchainlock.io/api/eagle-pms`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-booking-orders.md) for the provider-specific parameters and requirements.

