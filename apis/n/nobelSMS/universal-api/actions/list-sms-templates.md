# NobelSMS: List SMS Templates

Retrieves SMS templates from NobelSMS.

```
GET https://connect.mindcloud.co/v1/universal/nobelSMS/latest/actions/list-sms-templates
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a NobelSMS `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/nobelSMS/latest/actions/list-sms-templates?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/nobelSMS/latest/actions/list-sms-templates?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```



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

Through the native NobelSMS API, this operation is `GET /sms_template` (base URL `https://api.nobelsms.com/rest`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-sms-templates.md) for the provider-specific parameters and requirements.

