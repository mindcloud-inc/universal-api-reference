# Emporix Commerce Engine: Get Label

Retrieves a label from Emporix Commerce Engine.

```
GET https://connect.mindcloud.co/v1/universal/emporixCommerceEngine/latest/actions/get-label
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Emporix Commerce Engine `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/emporixCommerceEngine/latest/actions/get-label?connectionId=$CONNECTION_ID&labelId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "labelId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/emporixCommerceEngine/latest/actions/get-label?${params}`, {
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
| `labelId` | string | yes | The unique ID of the label. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "cloudinaryUrl": "https://example.com",
      "description": "string",
      "id": "string",
      "image": "string",
      "mediaId": "string",
      "metadata": {},
      "name": "Ava Chen",
      "overlay": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `cloudinaryUrl` | string |  |
| `description` | string |  |
| `id` | string |  |
| `image` | string |  |
| `mediaId` | string |  |
| `metadata` | object |  |
| `name` | string |  |
| `overlay` | object |  |

## Native endpoint

Through the native Emporix Commerce Engine API, this operation is `GET /labels/:labelId` (base URL `https://api.emporix.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-label.md) for the provider-specific parameters and requirements.

