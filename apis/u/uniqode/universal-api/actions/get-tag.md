# Uniqode: Get Tag

Retrieves a tag from your Uniqode account.

```
GET https://connect.mindcloud.co/v1/universal/uniqode/latest/actions/get-tag
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Uniqode `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/uniqode/latest/actions/get-tag?connectionId=$CONNECTION_ID&tagId=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "tagId": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/uniqode/latest/actions/get-tag?${params}`, {
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
| `tagId` | number | yes | The Uniqode tag ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "child_tags": [
        {}
      ],
      "color": "string",
      "created": "2026-05-07T12:00:00.000Z",
      "id": 1,
      "maintainer": 1,
      "name": "Ava Chen",
      "organization": 1,
      "product_type": "string",
      "qrcode_count": 1,
      "qrcode_data": [
        {}
      ],
      "qrcode_set": [
        {}
      ],
      "slug": "string",
      "updated": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `child_tags` | array<object> |  |
| `color` | string |  |
| `created` | date |  |
| `id` | number |  |
| `maintainer` | number |  |
| `name` | string |  |
| `organization` | number |  |
| `product_type` | string |  |
| `qrcode_count` | number |  |
| `qrcode_data` | array<object> |  |
| `qrcode_set` | array<object> |  |
| `slug` | string |  |
| `updated` | date |  |

## Native endpoint

Through the native Uniqode API, this operation is `GET /tags/:tagId/` (base URL `https://api.uniqode.com/api/2.0`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-tag.md) for the provider-specific parameters and requirements.

