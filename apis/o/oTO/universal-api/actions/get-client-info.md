# OTO: Get Client Info

Retrieves client information from the OTO API.

```
GET https://connect.mindcloud.co/v1/universal/oTO/latest/actions/get-client-info
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a OTO `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/oTO/latest/actions/get-client-info?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/oTO/latest/actions/get-client-info?${params}`, {
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
      "email": "ava@example.com",
      "name": "Ava Chen",
      "packageType": "string",
      "phone": "string",
      "remainingCredit": 1,
      "success": true,
      "validityDate": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `email` | string |  |
| `name` | string |  |
| `packageType` | string |  |
| `phone` | string |  |
| `remainingCredit` | number |  |
| `success` | boolean |  |
| `validityDate` | string |  |

## Native endpoint

Through the native OTO API, this operation is `GET /clientInfo` (base URL `https://api.tryoto.com/rest/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-client-info.md) for the provider-specific parameters and requirements.

