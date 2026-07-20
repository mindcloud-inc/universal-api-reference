# SimpleLocalize: Update Language

Updates an existing language in SimpleLocalize.

```
PUT https://connect.mindcloud.co/v1/universal/simpleLocalize/latest/actions/update-language
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a SimpleLocalize `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/simpleLocalize/latest/actions/update-language" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "languageKey": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/simpleLocalize/latest/actions/update-language', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "languageKey": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `languageKey` | string | yes |  |
| `key` | string | no |  |
| `name` | string | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "key": "string",
      "name": "Ava Chen"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `key` | string |  |
| `name` | string |  |

## Native endpoint

Through the native SimpleLocalize API, this operation is `PATCH /api/v1/languages/{languageKey}` (base URL `https://api.simplelocalize.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-language.md) for the provider-specific parameters and requirements.

