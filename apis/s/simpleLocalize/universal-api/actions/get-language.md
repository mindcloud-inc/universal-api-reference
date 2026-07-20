# SimpleLocalize: Get Language

Retrieves a language from SimpleLocalize.

```
GET https://connect.mindcloud.co/v1/universal/simpleLocalize/latest/actions/get-language
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a SimpleLocalize `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/simpleLocalize/latest/actions/get-language?connectionId=$CONNECTION_ID&languageKey=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "languageKey": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/simpleLocalize/latest/actions/get-language?${params}`, {
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
| `languageKey` | string | yes |  |

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

Through the native SimpleLocalize API, this operation is `GET /api/v1/languages/{languageKey}` (base URL `https://api.simplelocalize.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-language.md) for the provider-specific parameters and requirements.

