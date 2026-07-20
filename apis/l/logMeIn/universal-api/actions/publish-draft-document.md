# LogMeIn: Publish Draft Document

Publishes a draft document in LogMeIn.

```
PUT https://connect.mindcloud.co/v1/universal/logMeIn/latest/actions/publish-draft-document
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a LogMeIn `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/logMeIn/latest/actions/publish-draft-document" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "draftId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/logMeIn/latest/actions/publish-draft-document', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "draftId": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `draftId` | string | yes | Required draft ID to publish. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "documentId": "string",
      "id": "string",
      "publishedAt": "2026-05-07T12:00:00.000Z",
      "title": "string",
      "type": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `documentId` | string |  |
| `id` | string |  |
| `publishedAt` | date |  |
| `title` | string |  |
| `type` | string |  |

## Native endpoint

Through the native LogMeIn API, this operation is `POST /resolve/knowledge-base/v2/drafts/:draftId/publish` (base URL `https://api.goto.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/publish-draft-document.md) for the provider-specific parameters and requirements.

