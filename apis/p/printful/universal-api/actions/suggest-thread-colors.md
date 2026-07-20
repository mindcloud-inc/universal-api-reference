# Printful: Suggest Thread Colors

Retrieves suggested thread colors from an image in Printful.

```
GET https://connect.mindcloud.co/v1/universal/printful/latest/actions/suggest-thread-colors
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Printful `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/printful/latest/actions/suggest-thread-colors?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/printful/latest/actions/suggest-thread-colors?${params}`, {
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
      "hex": "string",
      "name": "Ava Chen"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `hex` | string |  |
| `name` | string |  |

## Native endpoint

Through the native Printful API, this operation is `POST /files/thread-colors` (base URL `https://api.printful.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/suggest-thread-colors.md) for the provider-specific parameters and requirements.

