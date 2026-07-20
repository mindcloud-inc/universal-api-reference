# Xperiencify: List Students

Retrieves students from Xperiencify with an optional course filter.

```
GET https://connect.mindcloud.co/v1/universal/xperiencify/latest/actions/list-students
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Xperiencify `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/xperiencify/latest/actions/list-students?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/xperiencify/latest/actions/list-students?${params}`, {
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
| `courseId` | number | no | Filter students by course. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "students": [
        [
          {}
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
| `students[]` | array<object> | Student rows returned by the list endpoint. This trial account currently returns an empty array, so nested student fields could not be confirmed from runtime. |

## Native endpoint

Through the native Xperiencify API, this operation is `GET /api/public/coach/students/` (base URL `https://api.xperiencify.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-students.md) for the provider-specific parameters and requirements.

