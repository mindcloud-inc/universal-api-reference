# Pixabay: Get Image by ID

Finds an image in Pixabay by ID.

```
GET https://connect.mindcloud.co/v1/universal/pixabay/latest/actions/get-image-by-id
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Pixabay `connectionId` ([setup](../authentication.md)).

This action also supports [filtering](../filtering.md) (`where`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/pixabay/latest/actions/get-image-by-id?connectionId=$CONNECTION_ID&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/pixabay/latest/actions/get-image-by-id?${params}`, {
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
| `id` | string | yes | Numeric Pixabay image ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "hits": [
        {}
      ],
      "total": 1,
      "totalHits": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `hits` | array<object> | Image results returned by Pixabay. |
| `total` | number | Total number of matches for the request. |
| `totalHits` | number | Accessible image results available through the API. |

## Native endpoint

Through the native Pixabay API, this operation is `GET /api/` (base URL `https://pixabay.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-image-by-id.md) for the provider-specific parameters and requirements.

