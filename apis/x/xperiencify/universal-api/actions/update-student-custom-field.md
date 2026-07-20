# Xperiencify: Update Student Custom Field

Updates a student custom field in Xperiencify.

```
PUT https://connect.mindcloud.co/v1/universal/xperiencify/latest/actions/update-student-custom-field
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Xperiencify `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/xperiencify/latest/actions/update-student-custom-field" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "student": "string",
  "field": "string",
  "value": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/xperiencify/latest/actions/update-student-custom-field', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "student": "string",
    "field": "string",
    "value": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `student` | string | yes | Student email address. |
| `field` | string | yes | Custom field name. |
| `value` | string | yes | Custom field value. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Xperiencify API returns.

## Native endpoint

Through the native Xperiencify API, this operation is `POST /api/public/student/customfield/` (base URL `https://api.xperiencify.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-student-custom-field.md) for the provider-specific parameters and requirements.

