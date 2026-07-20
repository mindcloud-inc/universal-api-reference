# Collected Notes: Get Site JSON



```
GET https://connect.mindcloud.co/v1/universal/collectedNotes/latest/actions/get-site-json
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Collected Notes `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/collectedNotes/latest/actions/get-site-json?connectionId=$CONNECTION_ID&sitePath=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "sitePath": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/collectedNotes/latest/actions/get-site-json?${params}`, {
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

## Response

```json
{
  "success": true,
  "data": [
    {
      "notes": [
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
      "site": {
        "about": "string",
        "createdAt": "2026-05-07T12:00:00.000Z",
        "domain": "string",
        "headline": "string",
        "host": "string",
        "id": 1,
        "name": "Ava Chen",
        "published": true,
        "sitePath": "string",
        "tinyletter": "string",
        "updatedAt": "2026-05-07T12:00:00.000Z",
        "userId": 1
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `notes[].body` | string |  |
| `notes[].createdAt` | date |  |
| `notes[].headline` | string |  |
| `notes[].id` | number |  |
| `notes[].path` | string |  |
| `notes[].siteId` | number |  |
| `notes[].title` | string |  |
| `notes[].updatedAt` | date |  |
| `notes[].url` | string |  |
| `notes[].userId` | number |  |
| `notes[].visibility` | string |  |
| `site.about` | string |  |
| `site.createdAt` | date |  |
| `site.domain` | string |  |
| `site.headline` | string |  |
| `site.host` | string |  |
| `site.id` | number |  |
| `site.name` | string |  |
| `site.published` | boolean |  |
| `site.sitePath` | string |  |
| `site.tinyletter` | string |  |
| `site.updatedAt` | date |  |
| `site.userId` | number |  |

## Native endpoint

Through the native Collected Notes API, this operation is `GET /:sitePath.json` (base URL `https://collectednotes.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-site-json.md) for the provider-specific parameters and requirements.

