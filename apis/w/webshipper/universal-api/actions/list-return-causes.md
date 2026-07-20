# Webshipper: List Return Causes

Retrieves return causes from Webshipper.

```
GET https://connect.mindcloud.co/v1/universal/webshipper/latest/actions/list-return-causes
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Webshipper `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/webshipper/latest/actions/list-return-causes?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/webshipper/latest/actions/list-return-causes?${params}`, {
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
      "description": "string",
      "id": "string",
      "limit_refund_methods": true,
      "name": "Ava Chen",
      "require_comment": true,
      "support_image_required": true,
      "type": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `description` | string |  |
| `id` | string |  |
| `limit_refund_methods` | boolean |  |
| `name` | string |  |
| `require_comment` | boolean |  |
| `support_image_required` | boolean |  |
| `type` | string |  |

## Native endpoint

Through the native Webshipper API, this operation is `GET /return_causes` (base URL `https://{{credentials.accountName}}.api.webshipper.io/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-return-causes.md) for the provider-specific parameters and requirements.

