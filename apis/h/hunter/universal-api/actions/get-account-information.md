# Hunter: Get Account Information



```
GET https://connect.mindcloud.co/v1/universal/hunter/latest/actions/get-account-information
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Hunter `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/hunter/latest/actions/get-account-information?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/hunter/latest/actions/get-account-information?${params}`, {
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
      "calls": {},
      "email": "ava@example.com",
      "firstName": "Ava",
      "lastName": "Chen",
      "planLevel": 1,
      "planName": "Ava Chen",
      "requests": {},
      "resetDate": "string",
      "teamId": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `calls` | object |  |
| `email` | string |  |
| `firstName` | string |  |
| `lastName` | string |  |
| `planLevel` | number |  |
| `planName` | string |  |
| `requests` | object |  |
| `resetDate` | string |  |
| `teamId` | number |  |

## Native endpoint

Through the native Hunter API, this operation is `GET /account` (base URL `https://api.hunter.io/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-account-information.md) for the provider-specific parameters and requirements.

