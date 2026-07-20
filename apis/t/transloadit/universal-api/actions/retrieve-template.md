# Transloadit: Retrieve Template

Retrieves a template by ID from Transloadit.

```
GET https://connect.mindcloud.co/v1/universal/transloadit/latest/actions/retrieve-template
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Transloadit `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/transloadit/latest/actions/retrieve-template?connectionId=$CONNECTION_ID&templateId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "templateId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/transloadit/latest/actions/retrieve-template?${params}`, {
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
| `templateId` | string | yes | The ID of the template to retrieve. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "content": {},
      "id": "string",
      "message": "string",
      "name": "Ava Chen",
      "ok": "string",
      "require_signature_auth": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `content` | object | Template content definition. |
| `id` | string | Template ID. |
| `message` | string | Human-readable result message. |
| `name` | string | Template name. |
| `ok` | string | Status code returned by Transloadit for template retrieval. |
| `require_signature_auth` | number | Whether signature auth is required for the template. |

## Native endpoint

Through the native Transloadit API, this operation is `GET /templates/:templateId` (base URL `https://api2.transloadit.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/retrieve-template.md) for the provider-specific parameters and requirements.

