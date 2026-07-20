# Metance: Get Current Session

Retrieves the current session from Metance.

```
GET https://connect.mindcloud.co/v1/universal/metance/latest/actions/get-current-session
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Metance `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/metance/latest/actions/get-current-session?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/metance/latest/actions/get-current-session?${params}`, {
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
      "departmentName": "Ava Chen",
      "email": "ava@example.com",
      "id": 1,
      "name": "Ava Chen",
      "title": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `departmentName` | string | Department name |
| `email` | string | Member email |
| `id` | number | Member ID |
| `name` | string | Member name |
| `title` | string | Member title |

## Native endpoint

Through the native Metance API, this operation is `GET /master/currentsession` (base URL `https://api.metance.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-current-session.md) for the provider-specific parameters and requirements.

