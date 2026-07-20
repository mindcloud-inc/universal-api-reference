# KeyVox: Unlock Locker

Unlocks an existing locker in KeyVox.

```
PUT https://connect.mindcloud.co/v1/universal/keyVox/latest/actions/unlock-locker
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a KeyVox `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/keyVox/latest/actions/unlock-locker" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/keyVox/latest/actions/unlock-locker', {
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
      "code": "string",
      "msg": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `code` | string | 0\:正常終了，0以外\:異常終了 |
| `msg` | string | レスポンスメッセージ |

## Native endpoint

Through the native KeyVox API, this operation is `POST /v1/unlockLocker` (base URL `https://eco.blockchainlock.io/api/eagle-pms`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/unlock-locker.md) for the provider-specific parameters and requirements.

