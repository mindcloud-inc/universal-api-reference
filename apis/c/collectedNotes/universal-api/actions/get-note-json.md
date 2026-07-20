# Collected Notes: Get Note JSON



```
GET https://connect.mindcloud.co/v1/universal/collectedNotes/latest/actions/get-note-json
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Collected Notes `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/collectedNotes/latest/actions/get-note-json?connectionId=$CONNECTION_ID&sitePath=string&notePath=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "sitePath": "string",
  "notePath": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/collectedNotes/latest/actions/get-note-json?${params}`, {
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
| `sitePath` | string | yes |  |
| `notePath` | string | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "body": "string",
      "createdAt": "2026-05-07T12:00:00.000Z",
      "headline": "string",
      "id": 1,
      "path": "string",
      "siteId": 1,
      "title": "string",
      "updatedAt": "2026-05-07T12:00:00.000Z",
      "url": "https://example.com",
      "userId": 1,
      "visibility": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `body` | string |  |
| `createdAt` | date |  |
| `headline` | string |  |
| `id` | number |  |
| `path` | string |  |
| `siteId` | number |  |
| `title` | string |  |
| `updatedAt` | date |  |
| `url` | string |  |
| `userId` | number |  |
| `visibility` | string |  |

## Native endpoint

Through the native Collected Notes API, this operation is `GET /:sitePath/:notePath.json` (base URL `https://collectednotes.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-note-json.md) for the provider-specific parameters and requirements.

