# PixelBin.io: List Transformation Modules

Retrieves transformation modules from the PixelBin.io playground.

```
GET https://connect.mindcloud.co/v1/universal/pixelBinio/latest/actions/list-transformation-modules
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a PixelBin.io `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/pixelBinio/latest/actions/list-transformation-modules?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/pixelBinio/latest/actions/list-transformation-modules?${params}`, {
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
      "delimiters": {},
      "plugins": [
        {}
      ],
      "presets": [
        {}
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `delimiters` | object | Transformation pattern delimiters. |
| `plugins` | array<object> | Available transformation modules. |
| `presets` | array<object> | Available transformation presets. |

## Native endpoint

Through the native PixelBin.io API, this operation is `GET /service/platform/assets/v1.0/playground/plugins` (base URL `https://api.pixelbin.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-transformation-modules.md) for the provider-specific parameters and requirements.

