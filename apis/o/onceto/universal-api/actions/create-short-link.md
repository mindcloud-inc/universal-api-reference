# Once.to: Create Short Link

Creates a new short link in Once.to.

```
POST https://connect.mindcloud.co/v1/universal/onceto/latest/actions/create-short-link
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Once.to `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/onceto/latest/actions/create-short-link" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "targetUrl": "https://example.com/offer"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/onceto/latest/actions/create-short-link', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "targetUrl": "https://example.com/offer"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `targetUrl` | string | yes | URL to redirect to. Example: `https://example.com/offer`. |
| `title` | string | no | Optional link title. Example: `Spring campaign`. |

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

Through the native Once.to API, this operation is `POST /links` (base URL `https://once.to/api/public/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-short-link.md) for the provider-specific parameters and requirements.

