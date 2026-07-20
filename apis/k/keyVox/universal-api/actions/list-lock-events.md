# KeyVox: List Lock Events

Lists lock events in your KeyVox account.

```
GET https://connect.mindcloud.co/v1/universal/keyVox/latest/actions/list-lock-events
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a KeyVox `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/keyVox/latest/actions/list-lock-events?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/keyVox/latest/actions/list-lock-events?${params}`, {
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
      "list": [
        {
          "id": "string",
          "uid": "string",
          "uname": "Ava Chen",
          "uphone": "string"
        }
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `list[].id` | string | ログID |
| `list[].uid` | string | ユーザーID |
| `list[].uname` | string | ユーザー名 |
| `list[].uphone` | string | ユーザー電話番号 |

## Native endpoint

Through the native KeyVox API, this operation is `POST /v1/locks/events` (base URL `https://eco.blockchainlock.io/api/eagle-pms`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-lock-events.md) for the provider-specific parameters and requirements.

