# GoCanvas: List Reference Images



```
GET https://connect.mindcloud.co/v1/universal/goCanvas/latest/actions/list-reference-images
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a GoCanvas `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/goCanvas/latest/actions/list-reference-images?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/goCanvas/latest/actions/list-reference-images?${params}`, {
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

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `formId` | number | no | Restrict results to images used by this assigned form. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "filename": "Ava Chen",
      "id": 1,
      "type": "string",
      "version": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `filename` | string |  |
| `id` | number |  |
| `type` | string |  |
| `version` | number |  |

## Native endpoint

Through the native GoCanvas API, this operation is `GET /reference_images` (base URL `https://www.gocanvas.com/api/v3`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-reference-images.md) for the provider-specific parameters and requirements.

