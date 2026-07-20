# Control D: Get User Data

Retrieves user data from Control D.

```
GET https://connect.mindcloud.co/v1/universal/controlD/latest/actions/get-user-data
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Control D `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/controlD/latest/actions/get-user-data?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/controlD/latest/actions/get-user-data?${params}`, {
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
      "date": "string",
      "email": "ava@example.com",
      "email_status": 1,
      "last_active": 1,
      "PK": "string",
      "proxy_access": 1,
      "status": 1,
      "twofa": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `date` | string |  |
| `email` | string |  |
| `email_status` | number |  |
| `last_active` | number |  |
| `PK` | string |  |
| `proxy_access` | number |  |
| `status` | number |  |
| `twofa` | number |  |

## Native endpoint

Through the native Control D API, this operation is `GET /users` (base URL `https://api.controld.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-user-data.md) for the provider-specific parameters and requirements.

