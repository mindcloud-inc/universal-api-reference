# Teach 'n Go: Enrol Prospect in Lesson

Enrols a prospect in a Teach 'n Go lesson.

```
POST https://connect.mindcloud.co/v1/universal/teachNGo/latest/actions/enrol-prospect-in-lesson
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Teach 'n Go `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/teachNGo/latest/actions/enrol-prospect-in-lesson" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "lessonId": "string",
  "prospectId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/teachNGo/latest/actions/enrol-prospect-in-lesson', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "lessonId": "string",
    "prospectId": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `lessonId` | string | yes | The Teach 'n Go lesson ID to enrol the prospect into. |
| `prospectId` | string | yes | The prospect ID to enrol. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "message": "string",
      "status": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `message` | string | Provider enrollment confirmation message. |
| `status` | boolean | Whether the enrollment succeeded. |

## Native endpoint

Through the native Teach 'n Go API, this operation is `POST /globalApis/enrollProspect` (base URL `https://app.teachngo.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/enrol-prospect-in-lesson.md) for the provider-specific parameters and requirements.

