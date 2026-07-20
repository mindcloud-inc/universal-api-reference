# NobelSMS: Get SMS Template

Retrieves an SMS template from NobelSMS by ID.

```
GET https://connect.mindcloud.co/v1/universal/nobelSMS/latest/actions/get-sms-template
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a NobelSMS `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/nobelSMS/latest/actions/get-sms-template?connectionId=$CONNECTION_ID&id=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/nobelSMS/latest/actions/get-sms-template?${params}`, {
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
| `id` | number | yes | Template ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "action_url": "https://example.com",
      "button_text": "string",
      "content": "string",
      "created": "string",
      "id": 1,
      "im_content": "string",
      "image_url": "https://example.com",
      "name": "Ava Chen",
      "sender_id": "string",
      "updated": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `action_url` | string |  |
| `button_text` | string |  |
| `content` | string |  |
| `created` | string |  |
| `id` | number |  |
| `im_content` | string |  |
| `image_url` | string |  |
| `name` | string |  |
| `sender_id` | string |  |
| `updated` | string |  |

## Native endpoint

Through the native NobelSMS API, this operation is `GET /sms_template/:id` (base URL `https://api.nobelsms.com/rest`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-sms-template.md) for the provider-specific parameters and requirements.

