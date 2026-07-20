# Zahara: List Users (Business Unit)

Retrieves users from a Zahara business unit.

```
GET https://connect.mindcloud.co/v1/universal/zahara/latest/actions/list-users-business-unit
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Zahara `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/zahara/latest/actions/list-users-business-unit?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/zahara/latest/actions/list-users-business-unit?${params}`, {
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
      "JobTitle": "string",
      "LastName": "Chen",
      "UserId": 1,
      "UserName": "Ava Chen"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `Email` | string | User email address. |
| `FirstName` | string | User first name. |
| `JobTitle` | string | User job title. |
| `LastName` | string | User last name. |
| `UserId` | number | Zahara user ID. |
| `UserName` | string | Zahara username. |

## Native endpoint

Through the native Zahara API, this operation is `GET /api/{{credentials.businessUnitApiKey}}/User/GetAll` (base URL `https://api.myzahara.net`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-users-business-unit.md) for the provider-specific parameters and requirements.

