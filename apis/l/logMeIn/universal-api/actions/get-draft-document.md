# LogMeIn: Get Draft Document

Retrieves a draft document from LogMeIn.

```
GET https://connect.mindcloud.co/v1/universal/logMeIn/latest/actions/get-draft-document
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a LogMeIn `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/logMeIn/latest/actions/get-draft-document?connectionId=$CONNECTION_ID&draftId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "draftId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/logMeIn/latest/actions/get-draft-document?${params}`, {
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
| `draftId` | string | yes | Required draft ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "content": "string",
      "id": "string",
      "lastModifiedAt": "2026-05-07T12:00:00.000Z",
      "title": "string",
      "type": "string",
      "visibility": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `content` | string |  |
| `id` | string |  |
| `lastModifiedAt` | date |  |
| `title` | string |  |
| `type` | string |  |
| `visibility` | string |  |

## Native endpoint

Through the native LogMeIn API, this operation is `GET /resolve/knowledge-base/v2/drafts/:draftId` (base URL `https://api.goto.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-draft-document.md) for the provider-specific parameters and requirements.

