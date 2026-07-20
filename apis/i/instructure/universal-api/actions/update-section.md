# Instructure: Update Section

Updates an existing section in Instructure Canvas.

```
PUT https://connect.mindcloud.co/v1/universal/instructure/latest/actions/update-section
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Instructure `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/instructure/latest/actions/update-section" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "id": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/instructure/latest/actions/update-section', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "id": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `id` | string | yes | Canvas section ID. |
| `sectionName` | string | no | Updated section name. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "course_id": "string",
      "id": "string",
      "name": "Ava Chen",
      "nonxlist_course_id": "string",
      "sis_section_id": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `course_id` | string |  |
| `id` | string |  |
| `name` | string |  |
| `nonxlist_course_id` | string |  |
| `sis_section_id` | string |  |

## Native endpoint

Through the native Instructure API, this operation is `PUT /sections/:id` (base URL `https://canvas.instructure.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-section.md) for the provider-specific parameters and requirements.

