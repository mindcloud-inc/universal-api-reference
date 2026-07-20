# Tettra: Suggest Page Update

Creates a page update suggestion in Tettra.

```
POST https://connect.mindcloud.co/v1/universal/tettra/latest/actions/suggest-page-update
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Tettra `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/tettra/latest/actions/suggest-page-update" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "pageId": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/tettra/latest/actions/suggest-page-update', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "pageId": 1
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `assignableId` | number | no | User ID to assign the suggestion to. |
| `description` | string | no | Suggested change details. |
| `pageId` | number | yes | Page ID to suggest updates for. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "success": true,
      "suggestionId": 1,
      "suggestionUrl": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `success` | boolean |  |
| `suggestionId` | number |  |
| `suggestionUrl` | string |  |

## Native endpoint

Through the native Tettra API, this operation is `POST /teams/85329/suggestions` (base URL `https://app.tettra.co/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/suggest-page-update.md) for the provider-specific parameters and requirements.

