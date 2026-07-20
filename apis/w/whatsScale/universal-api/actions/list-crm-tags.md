# WhatsScale: List CRM Tags

Retrieves CRM tags from your WhatsScale account.

```
GET https://connect.mindcloud.co/v1/universal/whatsScale/latest/actions/list-crm-tags
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a WhatsScale `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/whatsScale/latest/actions/list-crm-tags?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/whatsScale/latest/actions/list-crm-tags?${params}`, {
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
      "items": {
        "count": 1,
        "tag": "string"
      },
      "total": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `items` | array<object> |  |
| `items.count` | number |  |
| `items.tag` | string |  |
| `total` | number |  |

## Native endpoint

Through the native WhatsScale API, this operation is `GET /api/crm/tags` (base URL `https://proxy.whatsscale.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-crm-tags.md) for the provider-specific parameters and requirements.

