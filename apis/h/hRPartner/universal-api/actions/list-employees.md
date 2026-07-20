# HR Partner: List Employees



```
GET https://connect.mindcloud.co/v1/universal/hRPartner/latest/actions/list-employees
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a HR Partner `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/hRPartner/latest/actions/list-employees?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/hRPartner/latest/actions/list-employees?${params}`, {
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
      "code": "string",
      "email": "ava@example.com",
      "finishedAt": "2026-05-07T12:00:00.000Z",
      "firstNames": "Ava",
      "fullName": "Ava Chen",
      "id": 1,
      "isActive": true,
      "lastName": "Chen",
      "startedAt": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `code` | string |  |
| `email` | string |  |
| `finishedAt` | date |  |
| `firstNames` | string |  |
| `fullName` | string |  |
| `id` | number |  |
| `isActive` | boolean |  |
| `lastName` | string |  |
| `startedAt` | date |  |

## Native endpoint

Through the native HR Partner API, this operation is `GET /employees` (base URL `https://api.hrpartner.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-employees.md) for the provider-specific parameters and requirements.

