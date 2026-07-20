# ReachMail: Get Current User

Retrieves the current user from ReachMail.

```
GET https://connect.mindcloud.co/v1/universal/reachMail/latest/actions/get-current-user
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ReachMail `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/reachMail/latest/actions/get-current-user?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/reachMail/latest/actions/get-current-user?${params}`, {
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
      "AccountId": "string",
      "AccountKey": "string",
      "CompanyName": "Ava Chen",
      "Email": "ava@example.com",
      "Name": "Ava Chen",
      "Username": "Ava Chen"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `AccountId` | string |  |
| `AccountKey` | string |  |
| `CompanyName` | string |  |
| `Email` | string |  |
| `Name` | string |  |
| `Username` | string |  |

## Native endpoint

Through the native ReachMail API, this operation is `GET /Administration/Users/Current` (base URL `https://services.reachmail.net`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-current-user.md) for the provider-specific parameters and requirements.

