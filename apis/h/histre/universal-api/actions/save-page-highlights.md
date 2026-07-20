# Histre: Save Page Highlights

Creates page highlights in Histre.

```
POST https://connect.mindcloud.co/v1/universal/histre/latest/actions/save-page-highlights
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Histre `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/histre/latest/actions/save-page-highlights" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "url": "https://example.com",
  "title": "string",
  "text": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/histre/latest/actions/save-page-highlights', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "url": "https://example.com",
    "title": "string",
    "text": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `url` | string | yes | Page URL where the highlight was created. |
| `title` | string | yes | Title of the page where the highlight was created. |
| `text` | string | yes | Highlighted text to save. |
| `color` | string | no | Optional highlight color. |
| `tweet` | boolean | no | Optional flag indicating the highlight comes from a tweet. |
| `extra` | object | no | Optional object of extra highlight details. |
| `note` | string | no | Optional note text attached to the highlight. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Histre API returns.

## Native endpoint

Through the native Histre API, this operation is `POST /api/v1/highlight/` (base URL `https://histre.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/save-page-highlights.md) for the provider-specific parameters and requirements.

