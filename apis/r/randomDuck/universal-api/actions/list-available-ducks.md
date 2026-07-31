# Random Duck: List Available Ducks



```
GET https://connect.mindcloud.co/v1/universal/randomDuck/latest/actions/list-available-ducks
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Random Duck `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/randomDuck/latest/actions/list-available-ducks?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/randomDuck/latest/actions/list-available-ducks?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```



## Response

```json
{
  "success": true,
  "data": [
    {
      "gif_count": 1,
      "gifs": [
        "string"
      ],
      "http": [
        "string"
      ],
      "image_count": 1,
      "images": [
        "string"
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `gif_count` | number | Available GIF filename count. |
| `gifs` | array<string> | Available GIF filenames. |
| `http` | array<string> | Available HTTP-status duck JPEG filenames. |
| `image_count` | number | Available JPEG filename count. |
| `images` | array<string> | Available JPEG filenames. |

## Native endpoint

Through the native Random Duck API, this operation is `GET /list` (base URL `https://random-d.uk/api/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-available-ducks.md) for the provider-specific parameters and requirements.

