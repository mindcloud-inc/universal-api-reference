# AbcSubmit: Login

Authenticates a user in AbcSubmit.

```
GET https://connect.mindcloud.co/v1/universal/abcSubmit/latest/actions/login
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a AbcSubmit `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/abcSubmit/latest/actions/login?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/abcSubmit/latest/actions/login?${params}`, {
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
      "accessToken": "string",
      "exp": 1,
      "token": "string",
      "tokenType": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `accessToken` | string |  |
| `exp` | number |  |
| `token` | string |  |
| `tokenType` | string |  |

## Native endpoint

Through the native AbcSubmit API, this operation is `POST /api/v1/users/login` (base URL `https://www.abcsubmit.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/login.md) for the provider-specific parameters and requirements.

