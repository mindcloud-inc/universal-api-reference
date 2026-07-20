# Emporix Commerce Engine: Get Brand

Retrieves a brand from Emporix Commerce Engine.

```
GET https://connect.mindcloud.co/v1/universal/emporixCommerceEngine/latest/actions/get-brand
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Emporix Commerce Engine `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/emporixCommerceEngine/latest/actions/get-brand?connectionId=$CONNECTION_ID&brandId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "brandId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/emporixCommerceEngine/latest/actions/get-brand?${params}`, {
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
| `brandId` | string | yes | The unique ID of the brand to retrieve. |

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
      "localizedDescription": {},
      "localizedName": {},
      "mediaId": "string",
      "metadata": {},
      "name": "Ava Chen"
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
| `localizedDescription` | object |  |
| `localizedName` | object |  |
| `mediaId` | string |  |
| `metadata` | object |  |
| `name` | string |  |

## Native endpoint

Through the native Emporix Commerce Engine API, this operation is `GET /brand/brands/:brandId` (base URL `https://api.emporix.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-brand.md) for the provider-specific parameters and requirements.

