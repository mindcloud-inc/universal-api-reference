# Xperiencify: Remove Tags from Student

Deletes tags from a student in Xperiencify.

```
DELETE https://connect.mindcloud.co/v1/universal/xperiencify/latest/actions/remove-tags-from-student
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Xperiencify `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/xperiencify/latest/actions/remove-tags-from-student?connectionId=$CONNECTION_ID&studentEmail=ava%40example.com&tagNames=Ava%20Chen" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "studentEmail": "ava@example.com",
  "tagNames": "Ava Chen"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/xperiencify/latest/actions/remove-tags-from-student?${params}`, {
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
| `tags[]` | array<string> | Tag names returned after the remove request. |

## Native endpoint

Through the native Xperiencify API, this operation is `DELETE /api/public/student/tag/manager/` (base URL `https://api.xperiencify.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/remove-tags-from-student.md) for the provider-specific parameters and requirements.

