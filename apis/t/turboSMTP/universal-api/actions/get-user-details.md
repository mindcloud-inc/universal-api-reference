# turboSMTP: Get User Details

Retrieves your turboSMTP user account details.

```
GET https://connect.mindcloud.co/v1/universal/turboSMTP/latest/actions/get-user-details
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a turboSMTP `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/turboSMTP/latest/actions/get-user-details?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/turboSMTP/latest/actions/get-user-details?${params}`, {
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
      "accountID": 1,
      "active": true,
      "city": "string",
      "companyName": "Ava Chen",
      "country": "string",
      "email": "ava@example.com",
      "firstName": "Ava",
      "gateway": "string",
      "id": 1,
      "lastName": "Chen",
      "phone_number": "string",
      "timezone": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `accountID` | number |  |
| `active` | boolean |  |
| `city` | string |  |
| `companyName` | string |  |
| `country` | string |  |
| `email` | string |  |
| `firstName` | string |  |
| `gateway` | string |  |
| `id` | number |  |
| `lastName` | string |  |
| `phone_number` | string |  |
| `timezone` | string |  |

## Native endpoint

Through the native turboSMTP API, this operation is `GET /user` (base URL `https://pro.api.serversmtp.com/api/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-user-details.md) for the provider-specific parameters and requirements.

