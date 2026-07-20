# Once.to: Get Link

Retrieves a short link from Once.to.

```
GET https://connect.mindcloud.co/v1/universal/onceto/latest/actions/get-link
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Once.to `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/onceto/latest/actions/get-link?connectionId=$CONNECTION_ID&id=69cc19cf444c988c5fbf3759" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "69cc19cf444c988c5fbf3759"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/onceto/latest/actions/get-link?${params}`, {
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
| `id` | string | yes | ID of the short link to fetch. Example: `69cc19cf444c988c5fbf3759`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "active": true,
      "banned": true,
      "banTime": "2026-05-07T12:00:00.000Z",
      "botClicks": true,
      "clickCount": 1,
      "created": "2026-05-07T12:00:00.000Z",
      "customSlug": true,
      "expires": "2026-05-07T12:00:00.000Z",
      "failedCount": 1,
      "id": "string",
      "lastClicked": "2026-05-07T12:00:00.000Z",
      "ownerId": "string",
      "rules": {},
      "shortUrl": "https://example.com",
      "slug": "string",
      "starts": "2026-05-07T12:00:00.000Z",
      "statusCode": 1,
      "tags": [
        "string"
      ],
      "targetUrl": "https://example.com",
      "title": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `active` | boolean |  |
| `banned` | boolean |  |
| `banTime` | date |  |
| `botClicks` | boolean |  |
| `clickCount` | number |  |
| `created` | date |  |
| `customSlug` | boolean |  |
| `expires` | date |  |
| `failedCount` | number |  |
| `id` | string |  |
| `lastClicked` | date |  |
| `ownerId` | string |  |
| `rules` | object |  |
| `shortUrl` | string |  |
| `slug` | string |  |
| `starts` | date |  |
| `statusCode` | number |  |
| `tags` | array<string> |  |
| `targetUrl` | string |  |
| `title` | string |  |

## Native endpoint

Through the native Once.to API, this operation is `GET /links/:id` (base URL `https://once.to/api/public/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-link.md) for the provider-specific parameters and requirements.

