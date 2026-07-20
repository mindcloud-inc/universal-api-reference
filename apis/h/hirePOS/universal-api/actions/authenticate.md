# HirePOS: Authenticate

Validates API credentials for a HirePOS account.

```
GET https://connect.mindcloud.co/v1/universal/hirePOS/latest/actions/authenticate
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a HirePOS `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/hirePOS/latest/actions/authenticate?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/hirePOS/latest/actions/authenticate?${params}`, {
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
      "businessCode": "string",
      "businessName": "Ava Chen",
      "errorMessage": "string",
      "errorRaised": "string",
      "errorType": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `businessCode` | string |  |
| `businessName` | string |  |
| `errorMessage` | string |  |
| `errorRaised` | string |  |
| `errorType` | string |  |

## Native endpoint

Through the native HirePOS API, this operation is `GET /Authenticate` (base URL `https://api.hirepos.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/authenticate.md) for the provider-specific parameters and requirements.

