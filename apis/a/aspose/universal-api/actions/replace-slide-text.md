# Aspose: Replace Slide Text

Replaces text within a slide in Aspose.

```
PUT https://connect.mindcloud.co/v1/universal/aspose/latest/actions/replace-slide-text
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Aspose `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/aspose/latest/actions/replace-slide-text" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "name": "Ava Chen",
  "slideIndex": 1,
  "oldValue": "string",
  "newValue": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/aspose/latest/actions/replace-slide-text', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "name": "Ava Chen",
    "slideIndex": 1,
    "oldValue": "string",
    "newValue": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `name` | string | yes | The presentation file name. |
| `slideIndex` | number | yes | The 1-based slide index. |
| `oldValue` | string | yes | The text value to replace. |
| `newValue` | string | yes | The replacement text value. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Aspose API returns.

## Native endpoint

Through the native Aspose API, this operation is `POST /slides/:name/slides/:slideIndex/replaceText` (base URL `https://api.aspose.cloud/v3.0`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/replace-slide-text.md) for the provider-specific parameters and requirements.

