# KeyVox: Get Lock Card Status

Retrieves a lock card status from KeyVox.

```
GET https://connect.mindcloud.co/v1/universal/keyVox/latest/actions/get-lock-card-status
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a KeyVox `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/keyVox/latest/actions/get-lock-card-status?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/keyVox/latest/actions/get-lock-card-status?${params}`, {
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
      "status": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `status` | string | 10:作成準備中, 11:更新準備中, 12:削除準備中,<br> 20:作成中, 21:更新中, 22:削除中,<br> 30:作成済, 31:更新済, 32:削除済,<br> 90:作成エラー, 91:更新エラー, 92:削除エラー |

## Native endpoint

Through the native KeyVox API, this operation is `POST /v1/getCardStatus` (base URL `https://eco.blockchainlock.io/api/eagle-pms`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-lock-card-status.md) for the provider-specific parameters and requirements.

