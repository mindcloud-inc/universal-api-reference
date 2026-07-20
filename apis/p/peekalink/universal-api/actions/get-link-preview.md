# Peekalink: Get a Link Preview

Retrieves a link preview from Peekalink.

```
GET https://connect.mindcloud.co/v1/universal/peekalink/latest/actions/get-link-preview
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Peekalink `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/peekalink/latest/actions/get-link-preview?connectionId=$CONNECTION_ID&link=https%3A%2F%2Fwww.peekalink.io%2F" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "link": "https://www.peekalink.io/"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/peekalink/latest/actions/get-link-preview?${params}`, {
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
| `link` | string | yes | The URL to preview. Example: `https://www.peekalink.io/`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "description": "string",
      "domain": "string",
      "icon": {},
      "id": 1,
      "image": {},
      "ok": true,
      "page": {},
      "redirected": true,
      "requestId": "string",
      "size": 1,
      "status": 1,
      "title": "string",
      "type": "string",
      "updatedAt": "2026-05-07T12:00:00.000Z",
      "url": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `description` | string |  |
| `domain` | string |  |
| `icon` | object |  |
| `id` | number |  |
| `image` | object |  |
| `ok` | boolean |  |
| `page` | object |  |
| `redirected` | boolean |  |
| `requestId` | string |  |
| `size` | number |  |
| `status` | number |  |
| `title` | string |  |
| `type` | string |  |
| `updatedAt` | date |  |
| `url` | string |  |

## Native endpoint

Through the native Peekalink API, this operation is `POST /` (base URL `https://api.peekalink.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-link-preview.md) for the provider-specific parameters and requirements.

