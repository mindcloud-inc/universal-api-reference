# Classe365: List Students

Retrieves a list of students from Classe365.

```
GET https://connect.mindcloud.co/v1/universal/classe365/latest/actions/list-students
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Classe365 `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/classe365/latest/actions/list-students?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/classe365/latest/actions/list-students?${params}`, {
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
      "admissionNumber": "string",
      "firstName": "Ava",
      "id": "string",
      "lastName": "Chen",
      "studentEmail": "ava@example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `admissionNumber` | string |  |
| `firstName` | string |  |
| `id` | string |  |
| `lastName` | string |  |
| `studentEmail` | string |  |

## Native endpoint

Through the native Classe365 API, this operation is `GET /rest/studentsData` (base URL `https://{{credentials.username}}.classe365.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-students.md) for the provider-specific parameters and requirements.

