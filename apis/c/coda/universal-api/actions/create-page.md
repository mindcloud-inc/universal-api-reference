# Coda: Create Page

Creates a new page in a Coda doc.

```
POST https://connect.mindcloud.co/v1/universal/coda/latest/actions/create-page
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Coda `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/coda/latest/actions/create-page" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "docId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/coda/latest/actions/create-page', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "docId": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `docId` | list | yes |  |
| `name` | string | no |  |
| `subtitle` | string | no |  |
| `iconName` | string | no |  |
| `imageUrl` | string | no |  |
| `parentPageId` | string | no |  |
| `pageContent` | object | no |  |
| `pageContent.type` | string | no |  |
| `pageContent.canvasContent` | object | no |  |
| `pageContent.canvasContent.format` | string | no |  |
| `pageContent.canvasContent.content` | string | no |  |
| `pageContent.url` | string | no |  |
| `pageContent.renderMethod` | string | no |  |
| `pageContent.mode` | string | no |  |
| `pageContent.includeSubpages` | boolean | no |  |
| `pageContent.sourcePageId` | string | no |  |
| `pageContent.sourceDocId` | string | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "id": "string",
      "requestId": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `id` | string |  |
| `requestId` | string |  |

## Native endpoint

Through the native Coda API, this operation is `POST /docs/:docId/pages` (base URL `https://coda.io/apis/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-page.md) for the provider-specific parameters and requirements.

