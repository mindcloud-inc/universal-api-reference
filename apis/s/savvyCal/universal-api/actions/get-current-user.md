# SavvyCal: Get Current User



```
GET https://connect.mindcloud.co/v1/universal/savvyCal/latest/actions/get-current-user
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a SavvyCal `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/savvyCal/latest/actions/get-current-user?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/savvyCal/latest/actions/get-current-user?${params}`, {
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
      "avatarUrl": "https://example.com",
      "displayName": "Ava Chen",
      "email": "ava@example.com",
      "firstDayOfWeek": 1,
      "firstName": "Ava",
      "id": "string",
      "lastName": "Chen",
      "plan": "string",
      "timeFormat": "string",
      "timeZone": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `avatarUrl` | string | Avatar image URL. |
| `displayName` | string | User display name. |
| `email` | string | User email address. |
| `firstDayOfWeek` | number | Index of the user's first day of the week. |
| `firstName` | string | User first name. |
| `id` | string | Unique SavvyCal user identifier. |
| `lastName` | string | User last name. |
| `plan` | string | Subscription plan. |
| `timeFormat` | string | Preferred time format. |
| `timeZone` | string | User time zone identifier. |

## Native endpoint

Through the native SavvyCal API, this operation is `GET /v1/me` (base URL `https://api.savvycal.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-current-user.md) for the provider-specific parameters and requirements.

