# ConvertAPI: Get User Info



```
GET https://connect.mindcloud.co/v1/universal/convertAPI/latest/actions/new-action1
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ConvertAPI `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/convertAPI/latest/actions/new-action1?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/convertAPI/latest/actions/new-action1?${params}`, {
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
      "active": true,
      "apiKey": 1,
      "conversionsConsumed": 1,
      "conversionsTotal": 1,
      "email": "ava@example.com",
      "fullName": "Ava Chen",
      "secondsLeft": 1,
      "secret": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `active` | boolean |  |
| `apiKey` | number |  |
| `conversionsConsumed` | number |  |
| `conversionsTotal` | number |  |
| `email` | string |  |
| `fullName` | string |  |
| `secondsLeft` | number |  |
| `secret` | string |  |

## Native endpoint

Through the native ConvertAPI API, this operation is `GET /user` (base URL `https://v2.convertapi.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/new-action1.md) for the provider-specific parameters and requirements.

