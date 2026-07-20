# Picky Assist: Get Status of All Templates



```
GET https://connect.mindcloud.co/v1/universal/pickyAssist/latest/actions/get-status-of-all-templates
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Picky Assist `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/pickyAssist/latest/actions/get-status-of-all-templates?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/pickyAssist/latest/actions/get-status-of-all-templates?${params}`, {
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
      "message": "string",
      "status": 1,
      "templates": [
        {
          "category": "string",
          "footer": "string",
          "header": "string",
          "message_type": "string",
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
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `message` | string |  |
| `status` | number |  |
| `templates[].category` | string |  |
| `templates[].footer` | string |  |
| `templates[].header` | string |  |
| `templates[].message_type` | string |  |
| `templates[].template_id` | string |  |
| `templates[].template_message[].language` | string |  |
| `templates[].template_message[].message` | string |  |
| `templates[].template_name` | string |  |
| `templates[].template_status` | string |  |

## Native endpoint

Through the native Picky Assist API, this operation is `POST /template-status` (base URL `https://app.pickyassist.com/api/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-status-of-all-templates.md) for the provider-specific parameters and requirements.

