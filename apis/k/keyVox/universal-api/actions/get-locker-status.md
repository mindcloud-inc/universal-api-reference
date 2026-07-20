# KeyVox: Get Locker Status

Retrieves a locker status from KeyVox.

```
GET https://connect.mindcloud.co/v1/universal/keyVox/latest/actions/get-locker-status
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a KeyVox `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/keyVox/latest/actions/get-locker-status?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/keyVox/latest/actions/get-locker-status?${params}`, {
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
      "boxName": "Ava Chen",
      "boxNum": "string",
      "deviceId": "string",
      "status": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `boxName` | string | WEB管理画面「BACS」で設定したスマートロッカーの名前を指定する値が返却されます |
| `boxNum` | string | ボックスの番号情報が"00-01"のような書式で返却されます。00は副キャビネット番号、01はBOX番号を表します。<br> getLockerStatusのレスポンスでboxNumを確認することができます |
| `deviceId` | string | スマートロッカーを識別するユニークIDです |
| `status` | string | 0:未使用，1:利用中，2:期限切れ，9:故障 |

## Native endpoint

Through the native KeyVox API, this operation is `POST /v1/getLockerStatus` (base URL `https://eco.blockchainlock.io/api/eagle-pms`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-locker-status.md) for the provider-specific parameters and requirements.

