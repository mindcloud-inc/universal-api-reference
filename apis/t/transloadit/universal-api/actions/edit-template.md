# Transloadit: Edit Template

Updates an existing template in Transloadit.

```
PUT https://connect.mindcloud.co/v1/universal/transloadit/latest/actions/edit-template
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Transloadit `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/transloadit/latest/actions/edit-template" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "templateId": "string",
  "params": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/transloadit/latest/actions/edit-template', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "templateId": "string",
    "params": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `templateId` | string | yes | The ID of the template to edit. |
| `params` | string | yes | JSON string containing the updated Transloadit template definition. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "assembly_status_expiry": "string",
      "content": {},
      "id": "string",
      "message": "string",
      "name": "Ava Chen",
      "ok": "string",
      "require_signature_auth": 1,
      "transcoding_result_expiry": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `assembly_status_expiry` | string | Optional assembly status expiry timestamp, if configured. |
| `content` | object | Updated template definition content. |
| `id` | string | Template identifier. |
| `message` | string | Human-readable result message. |
| `name` | string | Template name. |
| `ok` | string | Status code returned by Transloadit for template update. |
| `require_signature_auth` | number | Whether signature authentication is required for this template. |
| `transcoding_result_expiry` | string | Optional transcoding result expiry timestamp, if configured. |

## Native endpoint

Through the native Transloadit API, this operation is `PUT /templates/:templateId` (base URL `https://api2.transloadit.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/edit-template.md) for the provider-specific parameters and requirements.

