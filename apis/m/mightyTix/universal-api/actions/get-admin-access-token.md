# Mighty Tix: Get Admin Access Token

Retrieves an admin access token from Mighty Tix.

```
GET https://connect.mindcloud.co/v1/universal/mightyTix/latest/actions/get-admin-access-token
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Mighty Tix `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/mightyTix/latest/actions/get-admin-access-token?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/mightyTix/latest/actions/get-admin-access-token?${params}`, {
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
      "account": {},
      "user": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `accessToken` | string |  |
| `account` | object |  |
| `user` | object |  |

## Native endpoint

Through the native Mighty Tix API, this operation is `POST admin-api/auth/login` (base URL `https://mindcloudmttix260403.mightytix.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-admin-access-token.md) for the provider-specific parameters and requirements.

