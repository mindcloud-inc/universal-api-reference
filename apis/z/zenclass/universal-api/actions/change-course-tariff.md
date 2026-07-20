# Zenclass: Change course tariff

Updates a student's course tariff in Zenclass.

```
PUT https://connect.mindcloud.co/v1/universal/zenclass/latest/actions/change-course-tariff
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Zenclass `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/zenclass/latest/actions/change-course-tariff" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "courseId": "string",
  "email": "ava@example.com",
  "tariffId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/zenclass/latest/actions/change-course-tariff', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "courseId": "string",
    "email": "ava@example.com",
    "tariffId": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `courseId` | string | yes | Zenclass course UUID. |
| `email` | string | yes | Student email address. |
| `tariffId` | string | yes | Course tariff UUID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "status": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `status` | boolean | Whether the tariff change succeeded. |

## Native endpoint

Through the native Zenclass API, this operation is `POST /api/v1/student/course/change_tariff` (base URL `https://api.zenclass.net`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/change-course-tariff.md) for the provider-specific parameters and requirements.

