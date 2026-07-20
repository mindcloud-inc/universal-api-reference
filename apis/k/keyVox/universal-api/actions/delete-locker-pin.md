# KeyVox: Delete Locker PIN

Deletes an existing locker PIN from KeyVox.

```
DELETE https://connect.mindcloud.co/v1/universal/keyVox/latest/actions/delete-locker-pin
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a KeyVox `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/keyVox/latest/actions/delete-locker-pin?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/keyVox/latest/actions/delete-locker-pin?${params}`, {
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

Through the native KeyVox API, this operation is `POST /v1/disableLockerPin` (base URL `https://eco.blockchainlock.io/api/eagle-pms`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-locker-pin.md) for the provider-specific parameters and requirements.

