# Typlog: Get Page

Retrieves a Typlog page by ID.

```
GET https://connect.mindcloud.co/v1/universal/typlog/latest/actions/get-page
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Typlog `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/typlog/latest/actions/get-page?connectionId=$CONNECTION_ID&id=1&siteId=4863" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "1",
  "siteId": "4863"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/typlog/latest/actions/get-page?${params}`, {
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
| `id` | number | yes | ID of the page. Example: `1`. |
| `siteId` | number | yes | Typlog site ID used to set the X-Site-Id header. Example: `4863`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "author": "string",
      "comment": "string",
      "content": "string",
      "createdAt": "2026-05-07T12:00:00.000Z",
      "format": "string",
      "id": 1,
      "lang": "string",
      "metadata": {},
      "publishedAt": "2026-05-07T12:00:00.000Z",
      "slug": "string",
      "status": "string",
      "subtitle": "string",
      "title": "string",
      "type": "string",
      "updatedAt": "2026-05-07T12:00:00.000Z",
      "url": "https://example.com",
      "visibility": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `author` | string |  |
| `comment` | string |  |
| `content` | string |  |
| `createdAt` | date |  |
| `format` | string |  |
| `id` | number |  |
| `lang` | string |  |
| `metadata` | object |  |
| `publishedAt` | date |  |
| `slug` | string |  |
| `status` | string |  |
| `subtitle` | string |  |
| `title` | string |  |
| `type` | string |  |
| `updatedAt` | date |  |
| `url` | string |  |
| `visibility` | string |  |

## Native endpoint

Through the native Typlog API, this operation is `GET /pages/[:id]` (base URL `https://api.typlog.com/v3`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-page.md) for the provider-specific parameters and requirements.

