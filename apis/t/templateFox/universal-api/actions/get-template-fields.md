# TemplateFox: Get Template Fields

Retrieves template fields from TemplateFox.

```
GET https://connect.mindcloud.co/v1/universal/templateFox/latest/actions/get-template-fields
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a TemplateFox `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/templateFox/latest/actions/get-template-fields?connectionId=$CONNECTION_ID&templateId=HMQywVpZxqAM" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "templateId": "HMQywVpZxqAM"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/templateFox/latest/actions/get-template-fields?${params}`, {
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
| `templateId` | string | yes | Template short ID (12 characters). Example: `HMQywVpZxqAM`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "helpText": "string",
      "key": "string",
      "label": "string",
      "required": true,
      "spec": [
        {}
      ],
      "type": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `helpText` | string |  |
| `key` | string |  |
| `label` | string |  |
| `required` | boolean |  |
| `spec` | array<object> |  |
| `type` | string |  |

## Native endpoint

Through the native TemplateFox API, this operation is `GET /v1/templates/{{template_id}}/fields` (base URL `https://api.templatefox.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-template-fields.md) for the provider-specific parameters and requirements.

