# iubenda: Get Subject

Retrieves a subject from iubenda.

```
GET https://connect.mindcloud.co/v1/universal/iubenda/latest/actions/get-subject
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a iubenda `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/iubenda/latest/actions/get-subject?connectionId=$CONNECTION_ID&subjectId=bd86b950-af4b-4a4f-9792-1690c18d42f1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "subjectId": "bd86b950-af4b-4a4f-9792-1690c18d42f1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/iubenda/latest/actions/get-subject?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as query string parameters ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `subjectId` | string | yes | Unique identifier of the subject Example: `bd86b950-af4b-4a4f-9792-1690c18d42f1`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "email": "ava@example.com",
      "first_name": "Ava",
      "full_name": "Ava Chen",
      "id": "string",
      "last_name": "Chen",
      "owner_id": "string",
      "phones": [
        "string"
      ],
      "preferences": {},
      "timestamp": "string",
      "verified": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `email` | string |  |
| `first_name` | string |  |
| `full_name` | string |  |
| `id` | string |  |
| `last_name` | string |  |
| `owner_id` | string |  |
| `phones` | array |  |
| `preferences` | object |  |
| `timestamp` | string |  |
| `verified` | boolean |  |

## Native endpoint

Through the native iubenda API, this operation is `GET /subjects/:id` (base URL `https://consent.iubenda.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-subject.md) for the provider-specific parameters and requirements.

