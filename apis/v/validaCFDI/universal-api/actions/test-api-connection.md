# ValidaCFDI: Test API Connection

Tests the API connection in ValidaCFDI.

```
GET https://connect.mindcloud.co/v1/universal/validaCFDI/latest/actions/test-api-connection
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ValidaCFDI `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/validaCFDI/latest/actions/test-api-connection?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/validaCFDI/latest/actions/test-api-connection?${params}`, {
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
      "authenticated": true,
      "email": "ava@example.com",
      "fullName": "Ava Chen",
      "message": "string",
      "planTier": "string",
      "userId": 1,
      "validationsRemaining": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `authenticated` | boolean |  |
| `email` | string |  |
| `fullName` | string |  |
| `message` | string |  |
| `planTier` | string |  |
| `userId` | number |  |
| `validationsRemaining` | number |  |

## Native endpoint

Through the native ValidaCFDI API, this operation is `GET /zapier/test` (base URL `https://api.valida-cfdi.com.mx/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/test-api-connection.md) for the provider-specific parameters and requirements.

