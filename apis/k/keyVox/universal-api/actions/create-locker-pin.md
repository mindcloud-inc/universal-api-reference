# KeyVox: Create Locker PIN

Creates a new locker PIN in KeyVox.

```
POST https://connect.mindcloud.co/v1/universal/keyVox/latest/actions/create-locker-pin
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a KeyVox `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/keyVox/latest/actions/create-locker-pin" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/keyVox/latest/actions/create-locker-pin', {
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



## Response

```json
{
  "success": true,
  "data": [
    {
      "pinCode": "string",
      "pinId": "string",
      "qrCode": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `pinCode` | string | スマートロッカーに配信される暗証番号(6桁)<br> ※ロック対象がBCL-XP1/BCL-XE1の場合、 pinCodeに数字が表示されます。パスワード開始日は3日以内であればすぐ配信されますが、3日以上であれば、DBに保存され、3日以内になってから配信されます。それ以外のロックの場合、アスタリスクが表示されます。pinIdより、getLockPinStatusを呼び出して、pinCodeを確認できます。パスワード開始日は3日以内であればすぐ発行されますが、3日以上であれば、DBに保存され、3日以内になってから発行されます。暗証番号が発行されるまで、pinCodeにアスタリスクが表示されます |
| `pinId` | string | 暗証番号を識別するユニークIDです |
| `qrCode` | string | 解錠用のQRコードを生成するための文字列です |

## Native endpoint

Through the native KeyVox API, this operation is `POST /v1/createLockerPin` (base URL `https://eco.blockchainlock.io/api/eagle-pms`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-locker-pin.md) for the provider-specific parameters and requirements.

