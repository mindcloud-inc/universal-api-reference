# Short.io: Update Link

Updates an existing link in Short.io.

```
PUT https://connect.mindcloud.co/v1/universal/shortio/latest/actions/update-link
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Short.io `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/shortio/latest/actions/update-link" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "linkId": "https://example.com"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/shortio/latest/actions/update-link', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "linkId": "https://example.com"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `linkId` | string | yes | Link ID. |
| `originalURL` | string | no | Original URL. |
| `path` | string | no | Link slug. |
| `title` | string | no | Link title. |
| `tags[]` | array<string> | no | Array of link tags. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `domainId` | string | no | Domain ID. |
| `ttl` | string | no | Time to live in milliseconds or ISO string. |
| `expiresAt` | string | no | Link expiration date in milliseconds or ISO string. |
| `redirectType` | number | no | HTTP redirect code. |
| `password` | string | no | Link password. |
| `cloaking` | boolean | no | Enable cloaking. |
| `clicksLimit` | number | no | Disable the link after this number of clicks. |
| `passwordContact` | boolean | no | Provide your email to users to get a password. |
| `skipQS` | boolean | no | Skip query string merging. |
| `archived` | boolean | no | Archive the link. |
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
| `tags` | array<string> |  |
| `title` | string |  |
| `updatedAt` | string |  |

## Native endpoint

Through the native Short.io API, this operation is `POST /links/:linkId` (base URL `https://api.short.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-link.md) for the provider-specific parameters and requirements.

