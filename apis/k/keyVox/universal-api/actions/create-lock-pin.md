# KeyVox: Create Lock PIN

Creates a new lock PIN in KeyVox.

```
POST https://connect.mindcloud.co/v1/universal/keyVox/latest/actions/create-lock-pin
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a KeyVox `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/keyVox/latest/actions/create-lock-pin" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/keyVox/latest/actions/create-lock-pin', {
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
| `pinCode` | string | スマートロックに配信される暗証番号です |
| `pinId` | string | 暗証番号を識別するユニークIDです |
| `qrCode` | string | 解錠用のQRコードを生成するための文字列です |

## Native endpoint

Through the native KeyVox API, this operation is `POST /v1/createLockPin` (base URL `https://eco.blockchainlock.io/api/eagle-pms`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-lock-pin.md) for the provider-specific parameters and requirements.

