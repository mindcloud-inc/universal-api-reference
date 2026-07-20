# Wooxy: Update Template

Updates an existing template in Wooxy.

```
PUT https://connect.mindcloud.co/v1/universal/wooxy/latest/actions/update-template
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Wooxy `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/wooxy/latest/actions/update-template" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "templateId": "69d68c4e4f47c8e4a60ee99f"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/wooxy/latest/actions/update-template', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "templateId": "69d68c4e4f47c8e4a60ee99f"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `templateId` | string | yes | The Wooxy template ID. Example: `69d68c4e4f47c8e4a60ee99f`. |
| `name` | string | no | Optional updated template name. Example: `Stage 3 Template Updated`. |
| `subject` | string | no | Optional updated email subject. Example: `Stage 3 Updated Subject`. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `html` | string | no | Optional updated HTML or text content. Example: `<html><body><h1>Stage 3 Updated</h1><p>Hello from Wooxy.</p></body></html>`. |

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

Through the native Wooxy API, this operation is `POST v3/template/email/update` (base URL `https://api.wooxy.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-template.md) for the provider-specific parameters and requirements.

