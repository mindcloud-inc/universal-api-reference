# Wooxy: Get Template

Retrieves a template from your Wooxy account.

```
GET https://connect.mindcloud.co/v1/universal/wooxy/latest/actions/get-template
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Wooxy `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/wooxy/latest/actions/get-template?connectionId=$CONNECTION_ID&templateId=69d68c4e4f47c8e4a60ee99f" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "templateId": "69d68c4e4f47c8e4a60ee99f"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/wooxy/latest/actions/get-template?${params}`, {
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
| `templateId` | string | yes | The Wooxy template ID. Example: `69d68c4e4f47c8e4a60ee99f`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "data": {
        "createdAt": "string",
        "html": "string",
        "name": "Ava Chen",
        "subject": "string",
        "templateId": "string",
        "templateSource": "string",
        "updatedAt": "string"
      },
      "errors": [
        "string"
      ],
      "result": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data.createdAt` | string |  |
| `data.html` | string |  |
| `data.name` | string |  |
| `data.subject` | string |  |
| `data.templateId` | string |  |
| `data.templateSource` | string |  |
| `data.updatedAt` | string |  |
| `errors` | array<string> |  |
| `result` | boolean |  |

## Native endpoint

Through the native Wooxy API, this operation is `POST v3/template/email/get` (base URL `https://api.wooxy.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-template.md) for the provider-specific parameters and requirements.

