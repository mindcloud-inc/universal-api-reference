# SimpleLocalize: List Translation Keys With Metadata

Retrieves translation keys with metadata from SimpleLocalize.

```
GET https://connect.mindcloud.co/v1/universal/simpleLocalize/latest/actions/list-translation-keys-with-metadata
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a SimpleLocalize `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/simpleLocalize/latest/actions/list-translation-keys-with-metadata?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/simpleLocalize/latest/actions/list-translation-keys-with-metadata?${params}`, {
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
| `key` | string | no |  |
| `namespace` | string | no |  |
| `sort` | list | no | One of: `created_at`, `deprecated_at`, `last_seen_at`, `modified_at`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "charactersLimit": 1,
      "codeDescription": "string",
      "createdAt": "string",
      "createdSource": "string",
      "description": "string",
      "key": "string",
      "lastSeenAt": "string",
      "lastSeenSource": "string",
      "namespace": "Ava Chen"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `charactersLimit` | number |  |
| `codeDescription` | string |  |
| `createdAt` | string |  |
| `createdSource` | string |  |
| `description` | string |  |
| `key` | string |  |
| `lastSeenAt` | string |  |
| `lastSeenSource` | string |  |
| `namespace` | string |  |

## Native endpoint

Through the native SimpleLocalize API, this operation is `GET /api/v1/translation-keys` (base URL `https://api.simplelocalize.io`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-translation-keys-with-metadata.md) for the provider-specific parameters and requirements.

