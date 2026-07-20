# KeyVox: Get Lock PIN Status

Retrieves a lock PIN status from KeyVox.

```
GET https://connect.mindcloud.co/v1/universal/keyVox/latest/actions/get-lock-pin-status
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a KeyVox `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/keyVox/latest/actions/get-lock-pin-status?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/keyVox/latest/actions/get-lock-pin-status?${params}`, {
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
      "pinCode": "string",
      "status": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `pinCode` | string | スマートロックに配信される暗証番号です |
| `status` | string | "暗証番号の配信状況を返却します<br> 10:create in queue, 11:change in queue, 12:disable in queue,<br>20:creating,<br> 21:changing, 22:disabling,<br>30:created, 31:changed, 32:disabled,<br>90:create<br> error, 91:change error, 92:disable error" |

## Native endpoint

Through the native KeyVox API, this operation is `POST /v1/getLockPinStatus` (base URL `https://eco.blockchainlock.io/api/eagle-pms`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-lock-pin-status.md) for the provider-specific parameters and requirements.

