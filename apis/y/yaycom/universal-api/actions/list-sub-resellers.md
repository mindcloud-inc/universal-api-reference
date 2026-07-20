# Yay.com: List Sub Resellers

Retrieves sub resellers from Yay.com.

```
GET https://connect.mindcloud.co/v1/universal/yaycom/latest/actions/list-sub-resellers
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Yay.com `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/yaycom/latest/actions/list-sub-resellers?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/yaycom/latest/actions/list-sub-resellers?${params}`, {
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
      "allowOutbound": true,
      "contactName": "Ava Chen",
      "name": "Ava Chen",
      "phone": "string",
      "storeFront": "string",
      "uuid": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `allowOutbound` | boolean |  |
| `contactName` | string |  |
| `name` | string |  |
| `phone` | string |  |
| `storeFront` | string |  |
| `uuid` | string |  |

## Native endpoint

Through the native Yay.com API, this operation is `GET /account/reseller` (base URL `https://api.yay.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-sub-resellers.md) for the provider-specific parameters and requirements.

