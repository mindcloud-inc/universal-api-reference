# eWeLink: Get User Information

Retrieves user information from eWeLink.

```
GET https://connect.mindcloud.co/v1/universal/eWeLink/latest/actions/get-user-information
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a eWeLink `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/eWeLink/latest/actions/get-user-information?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/eWeLink/latest/actions/get-user-information?${params}`, {
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
      "region": "string",
      "user": {
        "accountLevel": 1,
        "apikey": "string",
        "countryCode": "string",
        "email": "ava@example.com",
        "ipCountry": "string",
        "levelExpiredAt": 1,
        "nickname": "Ava Chen",
        "phoneNumber": "string"
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `region` | string |  |
| `user.accountLevel` | number |  |
| `user.apikey` | string |  |
| `user.countryCode` | string |  |
| `user.email` | string |  |
| `user.ipCountry` | string |  |
| `user.levelExpiredAt` | number |  |
| `user.nickname` | string |  |
| `user.phoneNumber` | string |  |

## Native endpoint

Through the native eWeLink API, this operation is `GET /v2/user/profile` (base URL `https://{{credentials.authorizeRequest.region}}-apia.coolkit.cc`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-user-information.md) for the provider-specific parameters and requirements.

