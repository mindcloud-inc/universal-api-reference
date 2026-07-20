# Xperiencify: List Student Tags

Retrieves tags for a student in Xperiencify.

```
GET https://connect.mindcloud.co/v1/universal/xperiencify/latest/actions/list-student-tags
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Xperiencify `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/xperiencify/latest/actions/list-student-tags?connectionId=$CONNECTION_ID&studentEmail=ava%40example.com" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "studentEmail": "ava@example.com"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/xperiencify/latest/actions/list-student-tags?${params}`, {
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
| `studentEmail` | string | yes | Email address for the student. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "tags": [
        [
          "string"
        ]
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `tags[]` | array<string> | Tag names associated with the student. |

## Native endpoint

Through the native Xperiencify API, this operation is `POST /api/public/student/tag/list/` (base URL `https://api.xperiencify.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-student-tags.md) for the provider-specific parameters and requirements.

