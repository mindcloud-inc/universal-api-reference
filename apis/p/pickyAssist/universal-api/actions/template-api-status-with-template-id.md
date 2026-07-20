# Picky Assist: Template API Status with Template ID



```
GET https://connect.mindcloud.co/v1/universal/pickyAssist/latest/actions/template-api-status-with-template-id
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Picky Assist `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/pickyAssist/latest/actions/template-api-status-with-template-id?connectionId=$CONNECTION_ID&template_id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "template_id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/pickyAssist/latest/actions/template-api-status-with-template-id?${params}`, {
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
| `template_id` | string | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "category": "string",
      "footer": "string",
      "message": "string",
      "message_type": "string",
      "status": 1,
      "template_id": "string",
      "template_message": [
        {
          "language": "string",
          "message": "string"
        }
      ],
      "template_name": "Ava Chen",
      "template_status": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `category` | string |  |
| `footer` | string |  |
| `message` | string |  |
| `message_type` | string |  |
| `status` | number |  |
| `template_id` | string |  |
| `template_message[].language` | string |  |
| `template_message[].message` | string |  |
| `template_name` | string |  |
| `template_status` | string |  |

## Native endpoint

Through the native Picky Assist API, this operation is `POST /template-status` (base URL `https://app.pickyassist.com/api/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/template-api-status-with-template-id.md) for the provider-specific parameters and requirements.

