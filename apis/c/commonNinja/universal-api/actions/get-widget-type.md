# Common Ninja: Get Widget Type

Retrieves a widget type from Common Ninja.

```
GET https://connect.mindcloud.co/v1/universal/commonNinja/latest/actions/get-widget-type
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Common Ninja `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/commonNinja/latest/actions/get-widget-type?connectionId=$CONNECTION_ID&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/commonNinja/latest/actions/get-widget-type?${params}`, {
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
| `id` | string | yes | The widget type ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "buttonText": "string",
      "categories": [
        "string"
      ],
      "id": "string",
      "logo": "string",
      "name": "Ava Chen",
      "promotionImage": "string",
      "slug": "string",
      "teaser": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `buttonText` | string |  |
| `categories` | array<string> |  |
| `id` | string |  |
| `logo` | string |  |
| `name` | string |  |
| `promotionImage` | string |  |
| `slug` | string |  |
| `teaser` | string |  |

## Native endpoint

Through the native Common Ninja API, this operation is `GET /widget-types/:id` (base URL `https://api.commoninja.com/platform/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-widget-type.md) for the provider-specific parameters and requirements.

