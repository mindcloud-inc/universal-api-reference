# Short.io: Create Link

Creates a new link in Short.io.

```
POST https://connect.mindcloud.co/v1/universal/shortio/latest/actions/create-link
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Short.io `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/shortio/latest/actions/create-link" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "originalURL": "https://example.com",
  "domain": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/shortio/latest/actions/create-link', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "originalURL": "https://example.com",
    "domain": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `originalURL` | string | yes | Original URL. |
| `domain` | string | yes | Domain hostname. |
| `path` | string | no | Custom link slug. |
| `title` | string | no | Link title. |
| `tags[]` | array<string> | no | Array of link tags. |
| `allowDuplicates` | boolean | no | Allow creating duplicate links for the same original URL. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `folderId` | string | no | Folder ID. |
| `ttl` | string | no | Time to live in milliseconds or ISO string. |
| `expiresAt` | string | no | Link expiration date in milliseconds or ISO string. |
| `redirectType` | number | no | HTTP redirect code. |
| `password` | string | no | Link password. |
| `cloaking` | boolean | no | Enable cloaking. |
| `clicksLimit` | number | no | Disable the link after this number of clicks. |
| `passwordContact` | boolean | no | Provide your email to users to get a password. |
| `skipQS` | boolean | no | Skip query string merging. |
| `archived` | boolean | no | Archive the link on creation. |
| `expiredURL` | string | no | URL to use after expiration. |
| `utmSource` | string | no | Set the utm_source parameter. |
| `utmMedium` | string | no | Set the utm_medium parameter. |
| `utmCampaign` | string | no | Set the utm_campaign parameter. |
| `utmTerm` | string | no | Set the utm_term parameter. |
| `utmContent` | string | no | Set the utm_content parameter. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "archived": true,
      "cloaking": true,
      "createdAt": "string",
      "displayPath": "string",
      "domainId": 1,
      "duplicate": true,
      "hasPassword": true,
      "id": "string",
      "idString": "string",
      "originalURL": "https://example.com",
      "ownerId": 1,
      "path": "string",
      "secureShortURL": "https://example.com",
      "shortURL": "https://example.com",
      "skipQS": true,
      "source": "string",
      "success": true,
      "tags": [
        "string"
      ],
      "title": "string",
      "updatedAt": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `archived` | boolean |  |
| `cloaking` | boolean |  |
| `createdAt` | string |  |
| `displayPath` | string |  |
| `domainId` | number |  |
| `duplicate` | boolean |  |
| `hasPassword` | boolean |  |
| `id` | string |  |
| `idString` | string |  |
| `originalURL` | string |  |
| `ownerId` | number |  |
| `path` | string |  |
| `secureShortURL` | string |  |
| `shortURL` | string |  |
| `skipQS` | boolean |  |
| `source` | string |  |
| `success` | boolean |  |
| `tags` | array<string> |  |
| `title` | string |  |
| `updatedAt` | string |  |

## Native endpoint

Through the native Short.io API, this operation is `POST /links` (base URL `https://api.short.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-link.md) for the provider-specific parameters and requirements.

