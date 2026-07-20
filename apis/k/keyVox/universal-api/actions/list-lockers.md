# KeyVox: List Lockers

Lists lockers in your KeyVox account.

```
GET https://connect.mindcloud.co/v1/universal/keyVox/latest/actions/list-lockers
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a KeyVox `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/keyVox/latest/actions/list-lockers?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/keyVox/latest/actions/list-lockers?${params}`, {
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
      "deviceId": "string",
      "deviceName": "Ava Chen"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `deviceId` | string | スマートロッカーを識別するユニークIDです |
| `deviceName` | string | WEB管理画面「BACS」で設定したスマートロッカーの名称です |

## Native endpoint

Through the native KeyVox API, this operation is `POST /v1/getLockers` (base URL `https://eco.blockchainlock.io/api/eagle-pms`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-lockers.md) for the provider-specific parameters and requirements.

