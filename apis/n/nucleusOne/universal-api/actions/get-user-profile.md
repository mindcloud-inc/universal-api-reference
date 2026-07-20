# Nucleus One: Get User Profile

Retrieves the current user profile from Nucleus One.

```
GET https://connect.mindcloud.co/v1/universal/nucleusOne/latest/actions/get-user-profile
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Nucleus One `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/nucleusOne/latest/actions/get-user-profile?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/nucleusOne/latest/actions/get-user-profile?${params}`, {
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
      "OTPSMSNumber": "string",
      "UserEmail": "ava@example.com",
      "UserName": "Ava Chen",
      "UserNameOverride": "Ava Chen",
      "UserPhone": "string",
      "UserProvider": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `OTPSMSNumber` | string |  |
| `UserEmail` | string |  |
| `UserName` | string |  |
| `UserNameOverride` | string |  |
| `UserPhone` | string |  |
| `UserProvider` | string |  |

## Native endpoint

Through the native Nucleus One API, this operation is `GET /user/profile` (base URL `https://client-api.nucleus.one/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-user-profile.md) for the provider-specific parameters and requirements.

