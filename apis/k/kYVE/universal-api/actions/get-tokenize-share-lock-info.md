# KYVE: Get Tokenize Share Lock Info



```
GET https://connect.mindcloud.co/v1/universal/kYVE/latest/actions/get-tokenize-share-lock-info
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a KYVE `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/kYVE/latest/actions/get-tokenize-share-lock-info?connectionId=$CONNECTION_ID&address=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "address": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/kYVE/latest/actions/get-tokenize-share-lock-info?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as query string parameters ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `address` | string | yes | Address to query tokenize share lock status for. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "expiration_time": "string",
      "status": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `expiration_time` | string |  |
| `status` | string |  |

## Native endpoint

Through the native KYVE API, this operation is `GET /kyve/liquid/v1beta1/tokenize_share_lock_info/{address}` (base URL `https://api.kyve.network`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-tokenize-share-lock-info.md) for the provider-specific parameters and requirements.

