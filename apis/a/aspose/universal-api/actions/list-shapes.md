# Aspose: List Shapes

Retrieves shapes from a slide in Aspose.

```
GET https://connect.mindcloud.co/v1/universal/aspose/latest/actions/list-shapes
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Aspose `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/aspose/latest/actions/list-shapes?connectionId=$CONNECTION_ID&name=Ava%20Chen&slideIndex=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "name": "Ava Chen",
  "slideIndex": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/aspose/latest/actions/list-shapes?${params}`, {
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
| `name` | string | yes | The presentation file name. |
| `slideIndex` | number | yes | The 1-based slide index. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Aspose API returns.

## Native endpoint

Through the native Aspose API, this operation is `GET /slides/:name/slides/:slideIndex/shapes` (base URL `https://api.aspose.cloud/v3.0`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-shapes.md) for the provider-specific parameters and requirements.

