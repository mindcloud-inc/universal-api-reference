# SendSafely: Get User Information



```
GET https://connect.mindcloud.co/v1/universal/sendSafely/latest/actions/get-user-information
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a SendSafely `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/sendSafely/latest/actions/get-user-information?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/sendSafely/latest/actions/get-user-information?${params}`, {
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
      "adminUser": true,
      "betaUser": true,
      "clientKey": "string",
      "email": "ava@example.com",
      "firstName": "Ava",
      "id": "string",
      "language": "string",
      "lastName": "Chen",
      "packageLife": 1,
      "publicKey": true,
      "response": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `adminUser` | boolean |  |
| `betaUser` | boolean |  |
| `clientKey` | string |  |
| `email` | string |  |
| `firstName` | string |  |
| `id` | string |  |
| `language` | string |  |
| `lastName` | string |  |
| `packageLife` | number |  |
| `publicKey` | boolean |  |
| `response` | string |  |

## Native endpoint

Through the native SendSafely API, this operation is `GET /user/` (base URL `https://app.sendsafely.com/api/v2.0`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-user-information.md) for the provider-specific parameters and requirements.

