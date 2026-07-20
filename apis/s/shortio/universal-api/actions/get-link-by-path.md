# Short.io: Get Link by Path

Retrieves link details from Short.io by path.

```
GET https://connect.mindcloud.co/v1/universal/shortio/latest/actions/get-link-by-path
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Short.io `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/shortio/latest/actions/get-link-by-path?connectionId=$CONNECTION_ID&domain=string&path=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "domain": "string",
  "path": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/shortio/latest/actions/get-link-by-path?${params}`, {
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
| `domain` | string | yes | Domain hostname. |
| `path` | string | yes | Link path. |

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

Through the native Short.io API, this operation is `GET /links/expand` (base URL `https://api.short.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-link-by-path.md) for the provider-specific parameters and requirements.

