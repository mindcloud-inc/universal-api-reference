# Hyperise: Create Short Link

Creates a personalized short link in Hyperise.

```
POST https://connect.mindcloud.co/v1/universal/hyperise/latest/actions/create-short-link
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Hyperise `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/hyperise/latest/actions/create-short-link" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "desc": "string",
  "imageHash": "string",
  "title": "string",
  "url": "https://example.com"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/hyperise/latest/actions/create-short-link', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "desc": "string",
    "imageHash": "string",
    "title": "string",
    "url": "https://example.com"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `businessName` | string | no | Optional personalization business name. |
| `desc` | string | yes | The Open Graph page description. |
| `email` | string | no | Optional personalization email. |
| `firstName` | string | no | Optional personalization first name. |
| `imageHash` | string | yes | The Hyperise image template hash. |
| `lastName` | string | no | Optional personalization last name. |
| `title` | string | yes | The Open Graph page title. |
| `url` | string | yes | The destination URL for the short link. |
| `website` | string | no | Optional personalization website. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "createdAt": "string",
      "desc": "string",
      "id": 1,
      "link": "https://example.com",
      "linkHash": "https://example.com",
      "title": "string",
      "updatedAt": "string",
      "url": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `createdAt` | string |  |
| `desc` | string |  |
| `id` | number |  |
| `link` | string |  |
| `linkHash` | string |  |
| `title` | string |  |
| `updatedAt` | string |  |
| `url` | string |  |

## Native endpoint

Through the native Hyperise API, this operation is `POST /short-links` (base URL `https://app.hyperise.io/api/v1/regular`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-short-link.md) for the provider-specific parameters and requirements.

