# Google Forms: Renew Form Watch

Renews a form watch in Google Forms for seven days.

```
PUT https://connect.mindcloud.co/v1/universal/googleForms/latest/actions/renew-form-watch
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Google Forms `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/googleForms/latest/actions/renew-form-watch" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "formId": "string",
  "watchId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/googleForms/latest/actions/renew-form-watch', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "formId": "string",
    "watchId": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `formId` | string | yes | The form identifier. |
| `watchId` | string | yes | The watch identifier. |

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

Through the native Google Forms API, this operation is `POST /:formId/watches/:watchId:renew` (base URL `https://forms.googleapis.com/v1/forms`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/renew-form-watch.md) for the provider-specific parameters and requirements.

