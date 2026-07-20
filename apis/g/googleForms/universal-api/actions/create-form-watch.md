# Google Forms: Create Form Watch

Creates a new seven-day form watch in Google Forms.

```
POST https://connect.mindcloud.co/v1/universal/googleForms/latest/actions/create-form-watch
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Google Forms `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/googleForms/latest/actions/create-form-watch" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "formId": "string",
  "eventType": "0",
  "topicName": "Ava Chen"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/googleForms/latest/actions/create-form-watch', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "formId": "string",
    "eventType": "0",
    "topicName": "Ava Chen"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `formId` | string | yes | The form identifier. |
| `eventType` | list | yes | Watch event type. Google currently supports schema changes. One of: `0`. |
| `topicName` | string | yes | Full Cloud Pub/Sub topic name that receives notifications. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `watchId` | string | no | Advanced: custom watch ID. Must be unused and 4-63 characters if provided. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "details": "string",
      "error": {
        "code": "string",
        "message": "string"
      },
      "message": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `details` | string |  |
| `error.code` | string |  |
| `error.message` | string |  |
| `message` | string |  |

## Native endpoint

Through the native Google Forms API, this operation is `POST /:formId/watches` (base URL `https://forms.googleapis.com/v1/forms`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-form-watch.md) for the provider-specific parameters and requirements.

