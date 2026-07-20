# Bitly: Get User

Retrieves the current authenticated Bitly user.

```
GET https://connect.mindcloud.co/v1/universal/bitly/latest/actions/get-user
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Bitly `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/bitly/latest/actions/get-user?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/bitly/latest/actions/get-user?${params}`, {
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
      "created": "string",
      "defaultGroupGuid": "string",
      "emails": [
        {
          "email": "ava@example.com",
          "isPrimary": true,
          "isVerified": true
        }
      ],
      "is2faEnabled": true,
      "isActive": true,
      "isSsoUser": true,
      "login": "string",
      "modified": "string",
      "name": "Ava Chen"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `created` | string |  |
| `defaultGroupGuid` | string |  |
| `emails[].email` | string |  |
| `emails[].isPrimary` | boolean |  |
| `emails[].isVerified` | boolean |  |
| `is2faEnabled` | boolean |  |
| `isActive` | boolean |  |
| `isSsoUser` | boolean |  |
| `login` | string |  |
| `modified` | string |  |
| `name` | string |  |

## Native endpoint

Through the native Bitly API, this operation is `GET /user` (base URL `https://api-ssl.bitly.com/v4`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-user.md) for the provider-specific parameters and requirements.

