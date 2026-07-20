# Communi App: Get Login Status



```
GET https://connect.mindcloud.co/v1/universal/communiApp/latest/actions/get-login-status
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Communi App `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/communiApp/latest/actions/get-login-status?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/communiApp/latest/actions/get-login-status?${params}`, {
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
      "device": "string",
      "group": 1,
      "id": 1,
      "logout": true,
      "sessionCheck": "string",
      "xhrToken": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `device` | string |  |
| `group` | number |  |
| `id` | number |  |
| `logout` | boolean |  |
| `sessionCheck` | string |  |
| `xhrToken` | string |  |

## Native endpoint

Through the native Communi App API, this operation is `GET /rest/login` (base URL `https://api.communiapp.de`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-login-status.md) for the provider-specific parameters and requirements.

