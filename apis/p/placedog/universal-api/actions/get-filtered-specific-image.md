# Placedog: Get Filtered Specific Image

Retrieves a filtered Placedog image by image ID.

```
GET https://connect.mindcloud.co/v1/universal/placedog/latest/actions/get-filtered-specific-image
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Placedog `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/placedog/latest/actions/get-filtered-specific-image?connectionId=$CONNECTION_ID&width=1&height=1&filter=0&imageId=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "width": "1",
  "height": "1",
  "filter": "0",
  "imageId": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/placedog/latest/actions/get-filtered-specific-image?${params}`, {
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
| `width` | number | yes |  |
| `height` | number | yes |  |
| `filter` | list | yes | One of: `0`, `1`, `2`, `3`, `4`, `5`, `6`. |
| `imageId` | number | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "data": [
        1
      ],
      "type": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data[]` | number |  |
| `type` | string |  |

## Native endpoint

Through the native Placedog API, this operation is `GET /[:width]/[:height]/[:filter]` (base URL `https://placedog.net`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-filtered-specific-image.md) for the provider-specific parameters and requirements.

