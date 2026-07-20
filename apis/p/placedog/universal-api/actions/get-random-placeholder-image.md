# Placedog: Get Random Placeholder Image

Retrieves a random placeholder dog image from Placedog.

```
GET https://connect.mindcloud.co/v1/universal/placedog/latest/actions/get-random-placeholder-image
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Placedog `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/placedog/latest/actions/get-random-placeholder-image?connectionId=$CONNECTION_ID&width=1&height=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "width": "1",
  "height": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/placedog/latest/actions/get-random-placeholder-image?${params}`, {
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

Through the native Placedog API, this operation is `GET /[:width]/[:height]` (base URL `https://placedog.net`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-random-placeholder-image.md) for the provider-specific parameters and requirements.

