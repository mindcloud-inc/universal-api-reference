# Collected Notes: Create Site



```
POST https://connect.mindcloud.co/v1/universal/collectedNotes/latest/actions/create-site
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Collected Notes `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/collectedNotes/latest/actions/create-site" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "site.name": "Ava Chen",
  "site.sitePath": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/collectedNotes/latest/actions/create-site', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "site.name": "Ava Chen",
    "site.sitePath": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `site` | object | no |  |
| `site.name` | string | yes |  |
| `site.sitePath` | string | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "about": "string",
      "createdAt": "2026-05-07T12:00:00.000Z",
      "domain": "string",
      "headline": "string",
      "host": "string",
      "id": 1,
      "isPremium": true,
      "name": "Ava Chen",
      "paymentPlatform": "string",
      "published": true,
      "sitePath": "string",
      "tinyletter": "string",
      "totalNotes": 1,
      "updatedAt": "2026-05-07T12:00:00.000Z",
      "userId": 1,
      "webhookUrl": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `about` | string |  |
| `createdAt` | date |  |
| `domain` | string |  |
| `headline` | string |  |
| `host` | string |  |
| `id` | number |  |
| `isPremium` | boolean |  |
| `name` | string |  |
| `paymentPlatform` | string |  |
| `published` | boolean |  |
| `sitePath` | string |  |
| `tinyletter` | string |  |
| `totalNotes` | number |  |
| `updatedAt` | date |  |
| `userId` | number |  |
| `webhookUrl` | string |  |

## Native endpoint

Through the native Collected Notes API, this operation is `POST /sites` (base URL `https://collectednotes.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-site.md) for the provider-specific parameters and requirements.

