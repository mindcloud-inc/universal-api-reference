# Zixflow: Get WhatsApp Template Variables

Retrieves WhatsApp template variables from Zixflow.

```
GET https://connect.mindcloud.co/v1/universal/zixflow/latest/actions/get-whatsapp-template-variables
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Zixflow `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/zixflow/latest/actions/get-whatsapp-template-variables?connectionId=$CONNECTION_ID&phoneId=string&templateName=Ava%20Chen&language=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "phoneId": "string",
  "templateName": "Ava Chen",
  "language": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/zixflow/latest/actions/get-whatsapp-template-variables?${params}`, {
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
| `phoneId` | string | yes | WhatsApp sender phone identifier from Zixflow WhatsApp Settings. |
| `templateName` | string | yes | WhatsApp template name, for example welcome_message. |
| `language` | string | yes | Template language code, for example en. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "data": [
        "string"
      ],
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
| `data` | array | Template variable rows returned by Zixflow. |
| `message` | string | Provider success or error message. |
| `status` | boolean | Whether the WhatsApp template-variable request succeeded. |

## Native endpoint

Through the native Zixflow API, this operation is `GET /campaign/whatsapp/variable-keys` (base URL `https://api.zixflow.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-whatsapp-template-variables.md) for the provider-specific parameters and requirements.

