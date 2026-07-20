# LogMeIn: Download Draft Document

Downloads a draft document from LogMeIn.

```
GET https://connect.mindcloud.co/v1/universal/logMeIn/latest/actions/download-draft-document
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a LogMeIn `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/logMeIn/latest/actions/download-draft-document?connectionId=$CONNECTION_ID&draftId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "draftId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/logMeIn/latest/actions/download-draft-document?${params}`, {
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
| `draftId` | string | yes | Required draft ID to download. |
| `inline` | boolean | no | Whether to display the file inline instead of downloading. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "contentType": "string",
      "fileName": "Ava Chen",
      "id": "string",
      "title": "string",
      "url": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `contentType` | string |  |
| `fileName` | string |  |
| `id` | string |  |
| `title` | string |  |
| `url` | string |  |

## Native endpoint

Through the native LogMeIn API, this operation is `GET /resolve/knowledge-base/v2/drafts/:draftId/download` (base URL `https://api.goto.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/download-draft-document.md) for the provider-specific parameters and requirements.

