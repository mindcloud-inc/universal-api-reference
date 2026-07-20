# SendPulse: List Templates

Retrieves a list of templates from SendPulse.

```
GET https://connect.mindcloud.co/v1/universal/sendPulse/latest/actions/list-templates
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a SendPulse `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/sendPulse/latest/actions/list-templates?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/sendPulse/latest/actions/list-templates?${params}`, {
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
      "category": "string",
      "category_info": [
        [
          "string"
        ]
      ],
      "created": "string",
      "id": "string",
      "is_structure": true,
      "lang": "string",
      "name": "Ava Chen",
      "name_slug": "Ava Chen",
      "owner": "string",
      "preview": "string",
      "real_id": 1,
      "tags": [
        [
          "string"
        ]
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `category` | string |  |
| `category_info[]` | array |  |
| `created` | string |  |
| `id` | string |  |
| `is_structure` | boolean |  |
| `lang` | string |  |
| `name` | string |  |
| `name_slug` | string |  |
| `owner` | string |  |
| `preview` | string |  |
| `real_id` | number |  |
| `tags[]` | array |  |

## Native endpoint

Through the native SendPulse API, this operation is `GET /templates` (base URL `https://api.sendpulse.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-templates.md) for the provider-specific parameters and requirements.

