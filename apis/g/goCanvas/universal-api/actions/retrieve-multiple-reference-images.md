# GoCanvas: Retrieve Multiple Reference Images



```
GET https://connect.mindcloud.co/v1/universal/goCanvas/latest/actions/retrieve-multiple-reference-images
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a GoCanvas `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/goCanvas/latest/actions/retrieve-multiple-reference-images?connectionId=$CONNECTION_ID&ids=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "ids": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/goCanvas/latest/actions/retrieve-multiple-reference-images?${params}`, {
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
| `ids` | number | yes | Image IDs to retrieve, supplied as repeated ids[] parameters; maximum 10 per request. Accepts multiple values as an array. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "data": "string",
      "id": 1,
      "type": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data` | string | Image content encoded as Base64. |
| `id` | number |  |
| `type` | string |  |

## Native endpoint

Through the native GoCanvas API, this operation is `GET /reference_images/bulk` (base URL `https://www.gocanvas.com/api/v3`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/retrieve-multiple-reference-images.md) for the provider-specific parameters and requirements.

