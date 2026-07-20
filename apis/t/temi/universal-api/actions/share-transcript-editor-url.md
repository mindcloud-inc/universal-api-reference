# Temi: Share Transcript Editor URL

Creates a shareable transcript editor URL in Temi.

```
POST https://connect.mindcloud.co/v1/universal/temi/latest/actions/share-transcript-editor-url
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Temi `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/temi/latest/actions/share-transcript-editor-url" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "id": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/temi/latest/actions/share-transcript-editor-url', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "id": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `id` | string | yes | Temi job identifier. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "editor_url": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `editor_url` | string | Shareable Temi transcript editor URL. |

## Native endpoint

Through the native Temi API, this operation is `POST /jobs/:id/share` (base URL `https://api.temi.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/share-transcript-editor-url.md) for the provider-specific parameters and requirements.

