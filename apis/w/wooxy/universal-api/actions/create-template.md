# Wooxy: Create Template

Creates a new template in Wooxy.

```
POST https://connect.mindcloud.co/v1/universal/wooxy/latest/actions/create-template
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Wooxy `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/wooxy/latest/actions/create-template" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "name": "Stage 3 Template",
  "subject": "Stage 3 Test Subject",
  "html": "<html><body><h1>Stage 3</h1><p>Hello from Wooxy.</p></body></html>"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/wooxy/latest/actions/create-template', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "name": "Stage 3 Template",
    "subject": "Stage 3 Test Subject",
    "html": "<html><body><h1>Stage 3</h1><p>Hello from Wooxy.</p></body></html>"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `name` | string | yes | The template name. Example: `Stage 3 Template`. |
| `subject` | string | yes | The email subject. Example: `Stage 3 Test Subject`. |
| `html` | string | yes | The full HTML or text content of the template. Example: `<html><body><h1>Stage 3</h1><p>Hello from Wooxy.</p></body></html>`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "errors": [
        "string"
      ],
      "result": true,
      "templateId": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `errors` | array<string> |  |
| `result` | boolean |  |
| `templateId` | string |  |

## Native endpoint

Through the native Wooxy API, this operation is `POST v3/template/email/create` (base URL `https://api.wooxy.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-template.md) for the provider-specific parameters and requirements.

