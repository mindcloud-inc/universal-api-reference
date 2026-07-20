# Inoreader: Get User Information

Retrieves the current user information from Inoreader.

```
GET https://connect.mindcloud.co/v1/universal/inoreader/latest/actions/get-user-information
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Inoreader `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/inoreader/latest/actions/get-user-information?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/inoreader/latest/actions/get-user-information?${params}`, {
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
      "isBloggerUser": true,
      "isMultiLoginEnabled": true,
      "signupTimeSec": 1,
      "userEmail": "ava@example.com",
      "userId": "string",
      "userName": "Ava Chen",
      "userProfileId": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `isBloggerUser` | boolean | Whether the account is marked as a blogger user. |
| `isMultiLoginEnabled` | boolean | Whether multi-login is enabled for the user. |
| `signupTimeSec` | number | The signup timestamp in Unix seconds. |
| `userEmail` | string | The email address on the connected Inoreader account. |
| `userId` | string | The Inoreader user identifier. |
| `userName` | string | The Inoreader username. |
| `userProfileId` | string | The profile identifier for the current user. |

## Native endpoint

Through the native Inoreader API, this operation is `GET /user-info` (base URL `https://www.inoreader.com/reader/api/0`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-user-information.md) for the provider-specific parameters and requirements.

