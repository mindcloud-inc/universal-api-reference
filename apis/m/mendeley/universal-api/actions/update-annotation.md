# Mendeley: Update Annotation



```
PUT https://connect.mindcloud.co/v1/universal/mendeley/latest/actions/update-annotation
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Mendeley `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/mendeley/latest/actions/update-annotation" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "id": "annotation id",
  "text": "Updated annotation text"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/mendeley/latest/actions/update-annotation', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "id": "annotation id",
    "text": "Updated annotation text"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `id` | string | yes | Identifier of the annotation. Example: `annotation id`. |
| `text` | string | yes | Updated annotation text content. Example: `Updated annotation text`. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Mendeley API returns.

## Native endpoint

Through the native Mendeley API, this operation is `PATCH /annotations/:id` (base URL `https://api.mendeley.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-annotation.md) for the provider-specific parameters and requirements.

