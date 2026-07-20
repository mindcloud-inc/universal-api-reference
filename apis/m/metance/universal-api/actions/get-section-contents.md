# Metance: Get Section Contents

Retrieves contents from a specific Metance section.

```
GET https://connect.mindcloud.co/v1/universal/metance/latest/actions/get-section-contents
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Metance `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/metance/latest/actions/get-section-contents?connectionId=$CONNECTION_ID&section=string&count=1&pageSize=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "section": "string",
  "count": "1",
  "pageSize": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/metance/latest/actions/get-section-contents?${params}`, {
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
| `section` | string | yes | Section name to load contents from, such as Home. |
| `count` | number | yes | Maximum number of contents to return. |
| `pageSize` | number | yes | Page size used by the Metance contents feed. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "answerCount": 1,
      "contentText": "string",
      "contentUrl": "https://example.com",
      "folderName": "Ava Chen",
      "id": 1,
      "name": "Ava Chen",
      "status": 1,
      "title": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `answerCount` | number | Answer count |
| `contentText` | string | Content text |
| `contentUrl` | string | Content URL slug |
| `folderName` | string | Folder name |
| `id` | number | Content ID |
| `name` | string | Content name |
| `status` | number | Content status |
| `title` | string | Content title |

## Native endpoint

Through the native Metance API, this operation is `GET /contents` (base URL `https://api.metance.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-section-contents.md) for the provider-specific parameters and requirements.

