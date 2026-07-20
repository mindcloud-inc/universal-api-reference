# Morningmate: Search Employees

Retrieves employees from Morningmate.

```
GET https://connect.mindcloud.co/v1/universal/morningmate/latest/actions/search-employees
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Morningmate `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/morningmate/latest/actions/search-employees?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/morningmate/latest/actions/search-employees?${params}`, {
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
      "cellPhoneNumber": "string",
      "companyPhoneNumber": "string",
      "divisionCode": "string",
      "divisionId": "string",
      "divisionName": "Ava Chen",
      "email": "ava@example.com",
      "fullname": "Ava Chen",
      "inttId": "string",
      "responsibility": "string",
      "userId": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `cellPhoneNumber` | string | Cell phone number |
| `companyPhoneNumber` | string | Company phone number |
| `divisionCode` | string | Division code |
| `divisionId` | string | Division ID |
| `divisionName` | string | Division name |
| `email` | string | Email address |
| `fullname` | string | Employee full name |
| `inttId` | string | Morningmate employee integration ID |
| `responsibility` | string | Employee responsibility or role |
| `userId` | string | Morningmate user ID |

## Native endpoint

Through the native Morningmate API, this operation is `GET /v1/employees` (base URL `https://api.morningmate.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/search-employees.md) for the provider-specific parameters and requirements.

