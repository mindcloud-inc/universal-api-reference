# Coda: Update Page

Updates a page in a Coda doc.

```
PUT https://connect.mindcloud.co/v1/universal/coda/latest/actions/update-page
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Coda `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/coda/latest/actions/update-page" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "docId": "string",
  "pageIdOrName": "Ava Chen"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/coda/latest/actions/update-page', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "docId": "string",
    "pageIdOrName": "Ava Chen"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `docId` | list | yes |  |
| `pageIdOrName` | list | yes |  |
| `name` | string | no |  |
| `subtitle` | string | no |  |
| `iconName` | string | no |  |
| `imageUrl` | string | no |  |
| `isHidden` | boolean | no |  |
| `contentUpdate` | object | no |  |
| `contentUpdate.insertionMode` | string | no |  |
| `contentUpdate.elementId` | string | no |  |
| `contentUpdate.canvasContent` | object | no |  |
| `contentUpdate.canvasContent.format` | string | no |  |
| `contentUpdate.canvasContent.content` | string | no |  |

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

Through the native Coda API, this operation is `PUT /docs/:docId/pages/:pageIdOrName` (base URL `https://coda.io/apis/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-page.md) for the provider-specific parameters and requirements.

