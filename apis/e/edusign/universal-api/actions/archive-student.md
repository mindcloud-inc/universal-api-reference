# Edusign: Archive Student

Archives an existing student in Edusign.

```
DELETE https://connect.mindcloud.co/v1/universal/edusign/latest/actions/archive-student
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Edusign `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/edusign/latest/actions/archive-student?connectionId=$CONNECTION_ID&studentId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "studentId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/edusign/latest/actions/archive-student?${params}`, {
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
| `studentId` | string | yes | Student ID |

## Response

```json
{
  "success": true,
  "data": [
    {
      "result": true,
      "status": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `result` | boolean |  |
| `status` | string |  |

## Native endpoint

Through the native Edusign API, this operation is `DELETE /v1/student/:studentId` (base URL `https://ext.edusign.fr`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/archive-student.md) for the provider-specific parameters and requirements.

