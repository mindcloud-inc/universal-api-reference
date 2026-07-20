# Wistia: Update Captions

Updates captions for a Wistia media language.

```
PUT https://connect.mindcloud.co/v1/universal/wistia/latest/actions/update-captions
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Wistia `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/wistia/latest/actions/update-captions" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "mediaHashedId": "string",
  "languageCode": "string",
  "text": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/wistia/latest/actions/update-captions', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "mediaHashedId": "string",
    "languageCode": "string",
    "text": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `mediaHashedId` | string | yes |  |
| `languageCode` | string | yes |  |
| `text` | string | yes |  |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Wistia API returns.

## Native endpoint

Through the native Wistia API, this operation is `PUT /modern/medias/:mediaHashedId/captions/:languageCode` (base URL `https://api.wistia.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-captions.md) for the provider-specific parameters and requirements.

