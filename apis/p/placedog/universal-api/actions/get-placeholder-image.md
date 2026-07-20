# Placedog: Get Placeholder Image

Retrieves a placeholder dog image from Placedog by width.

```
GET https://connect.mindcloud.co/v1/universal/placedog/latest/actions/get-placeholder-image
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Placedog `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/placedog/latest/actions/get-placeholder-image?connectionId=$CONNECTION_ID&width=500" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "width": "500"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/placedog/latest/actions/get-placeholder-image?${params}`, {
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
| `width` | number | yes | Image width from 1 to 1000. Example: `500`. |

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

Through the native Placedog API, this operation is `GET /[:width]` (base URL `https://placedog.net`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-placeholder-image.md) for the provider-specific parameters and requirements.

