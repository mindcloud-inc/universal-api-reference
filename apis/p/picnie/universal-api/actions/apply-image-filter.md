# Picnie: Apply Image Filter

Creates a filtered image in Picnie.

```
POST https://connect.mindcloud.co/v1/universal/picnie/latest/actions/apply-image-filter
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Picnie `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/picnie/latest/actions/apply-image-filter" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "imageUrl": "https://example.com",
  "filter": "IMG_FILTER_GRAYSCALE",
  "projectId": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/picnie/latest/actions/apply-image-filter', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "imageUrl": "https://example.com",
    "filter": "IMG_FILTER_GRAYSCALE",
    "projectId": 1
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `imageUrl` | string | yes | Image URL to filter. |
| `filter` | string | yes | Filter constant such as IMG_FILTER_GRAYSCALE. Default: `IMG_FILTER_GRAYSCALE`. |
| `projectId` | number | yes | Project ID that will own the filtered image. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "error": true,
      "message": "string",
      "url": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `error` | boolean |  |
| `message` | string |  |
| `url` | string |  |

## Native endpoint

Through the native Picnie API, this operation is `POST /filter-on-image` (base URL `https://picnie.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/apply-image-filter.md) for the provider-specific parameters and requirements.

