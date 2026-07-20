# SimpleLocalize: Update Translation Key by ID

Updates an existing translation key by ID in SimpleLocalize.

```
PUT https://connect.mindcloud.co/v1/universal/simpleLocalize/latest/actions/update-translation-key-by-id
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a SimpleLocalize `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/simpleLocalize/latest/actions/update-translation-key-by-id" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "id": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/simpleLocalize/latest/actions/update-translation-key-by-id', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "id": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `id` | string | yes |  |
| `key` | string | no |  |
| `namespace` | string | no |  |
| `description` | string | no |  |
| `codeDescription` | string | no |  |
| `charactersLimit` | number | no |  |
| `deprecated` | boolean | no |  |
| `lock` | boolean | no |  |
| `tags[]` | array<string> | no |  |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native SimpleLocalize API returns.

## Native endpoint

Through the native SimpleLocalize API, this operation is `PATCH /api/v1/translation-keys/{id}` (base URL `https://api.simplelocalize.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-translation-key-by-id.md) for the provider-specific parameters and requirements.

