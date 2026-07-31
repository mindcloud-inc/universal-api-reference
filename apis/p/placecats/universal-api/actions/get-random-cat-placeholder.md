# Placecats: Get Random Cat Placeholder



```
GET https://connect.mindcloud.co/v1/universal/placecats/latest/actions/get-random-cat-placeholder
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Placecats `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/placecats/latest/actions/get-random-cat-placeholder?connectionId=$CONNECTION_ID&width=1&height=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "width": "1",
  "height": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/placecats/latest/actions/get-random-cat-placeholder?${params}`, {
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
| `width` | number | yes | Required image width in pixels. |
| `height` | number | yes | Required image height in pixels. |
| `fit` | string | no | Optional fit: cover (default), contain, fill, inside, or outside. |
| `position` | string | no | Optional crop position: center (default), top, bottom, left, or right. |

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
| `data` | array<number> | Native platform Buffer byte sequence for the returned JPEG. |
| `type` | string | Native platform raw-response marker; runtime value is Buffer. |

## Native endpoint

Through the native Placecats API, this operation is `GET /:width/:height` (base URL `https://placecats.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-random-cat-placeholder.md) for the provider-specific parameters and requirements.

