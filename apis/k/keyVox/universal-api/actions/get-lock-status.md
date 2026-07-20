# KeyVox: Get Lock Status

Retrieves a lock status from KeyVox.

```
GET https://connect.mindcloud.co/v1/universal/keyVox/latest/actions/get-lock-status
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a KeyVox `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/keyVox/latest/actions/get-lock-status?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/keyVox/latest/actions/get-lock-status?${params}`, {
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
      "battery": "string",
      "pinType": "string",
      "relateBattery": "string",
      "relateType": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `battery` | string | バッテリー残量 |
| `pinType` | string | 暗証番号方式を指定します。<br> 1:オンライン方式, 2:オフライン方式, 3:暗証番号非対応<br> ※この項目が存在しない場合、[3:暗証番号非対応]として処理してください |
| `relateBattery` | string | BCL-QR1と連動して利用しているロックのバッテリー残量です<br> ※BCL-QR1と連動するロックがある場合のみ項目が返却されます |
| `relateType` | string | BCL-QR1と連動して利用しているロックのタイプです<br> ※BCL-QR1と連動するロックがある場合のみ項目が返却されます |

## Native endpoint

Through the native KeyVox API, this operation is `POST /v1/getLockStatus` (base URL `https://eco.blockchainlock.io/api/eagle-pms`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-lock-status.md) for the provider-specific parameters and requirements.

