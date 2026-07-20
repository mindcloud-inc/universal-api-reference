# Xperiencify: Add Tags to Student

Updates a student's tags in Xperiencify.

```
PUT https://connect.mindcloud.co/v1/universal/xperiencify/latest/actions/add-tags-to-student
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Xperiencify `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/xperiencify/latest/actions/add-tags-to-student" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "studentEmail": "ava@example.com",
  "tagNames": "Ava Chen"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/xperiencify/latest/actions/add-tags-to-student', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "studentEmail": "ava@example.com",
    "tagNames": "Ava Chen"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `studentEmail` | string | yes | Email address for the student. |
| `tagNames` | string | yes | One or more tag names separated by commas. |

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
| `tags[]` | array<string> | Tag names associated with the student after the update request. |

## Native endpoint

Through the native Xperiencify API, this operation is `POST /api/public/student/tag/manager/` (base URL `https://api.xperiencify.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/add-tags-to-student.md) for the provider-specific parameters and requirements.

