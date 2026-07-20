# Classe365: Change Student Status

Updates a student's status in Classe365.

```
PUT https://connect.mindcloud.co/v1/universal/classe365/latest/actions/change-student-status
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Classe365 `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/classe365/latest/actions/change-student-status" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/classe365/latest/actions/change-student-status', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `status` | string | no | Student status such as active or alumni. |
| `student_ids` | string | no | Comma-separated student ids. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "status": "string",
      "studentIds": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `status` | string |  |
| `studentIds` | string |  |

## Native endpoint

Through the native Classe365 API, this operation is `POST /rest/studentStatusUpdate` (base URL `https://{{credentials.username}}.classe365.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/change-student-status.md) for the provider-specific parameters and requirements.

