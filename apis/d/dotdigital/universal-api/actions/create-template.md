# Dotdigital: Create Template

Creates a new email campaign template in Dotdigital.

```
POST https://connect.mindcloud.co/v1/universal/dotdigital/latest/actions/create-template
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Dotdigital `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/dotdigital/latest/actions/create-template" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "name": "Ava Chen",
  "subject": "string",
  "fromName": "Ava Chen",
  "htmlContent": "string",
  "plainTextContent": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/dotdigital/latest/actions/create-template', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "name": "Ava Chen",
    "subject": "string",
    "fromName": "Ava Chen",
    "htmlContent": "string",
    "plainTextContent": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `name` | string | yes | The name of the template being created |
| `subject` | string | yes | The email subject line of the template |
| `fromName` | string | yes | The from name of the template |
| `htmlContent` | string | yes | The HTML content of the template |
| `plainTextContent` | string | yes | The plain text content of the template |

## Response

```json
{
  "success": true,
  "data": [
    {
      "fromName": "Ava Chen",
      "htmlContent": "string",
      "id": 1,
      "name": "Ava Chen",
      "plainTextContent": "string",
      "replyAction": "string",
      "replyToAddress": "string",
      "subject": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `fromName` | string |  |
| `htmlContent` | string |  |
| `id` | number |  |
| `name` | string |  |
| `plainTextContent` | string |  |
| `replyAction` | string |  |
| `replyToAddress` | string |  |
| `subject` | string |  |

## Native endpoint

Through the native Dotdigital API, this operation is `POST /v2/templates` (base URL `https://r2-api.dotmailer.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-template.md) for the provider-specific parameters and requirements.

