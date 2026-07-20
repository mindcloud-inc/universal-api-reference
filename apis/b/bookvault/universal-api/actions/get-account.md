# Bookvault: Get Account

Retrieves your account details from Bookvault.

```
GET https://connect.mindcloud.co/v1/universal/bookvault/latest/actions/get-account
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Bookvault `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/bookvault/latest/actions/get-account?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/bookvault/latest/actions/get-account?${params}`, {
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
      "Email": "ava@example.com",
      "FirstName": "Ava",
      "IsDisabled": true,
      "LastName": "Chen",
      "Phone": "string",
      "ProfileID": 1,
      "Role": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `Email` | string |  |
| `FirstName` | string |  |
| `IsDisabled` | boolean |  |
| `LastName` | string |  |
| `Phone` | string |  |
| `ProfileID` | number |  |
| `Role` | object |  |

## Native endpoint

Through the native Bookvault API, this operation is `GET /Account` (base URL `https://api.bookvault.app/v3`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-account.md) for the provider-specific parameters and requirements.

