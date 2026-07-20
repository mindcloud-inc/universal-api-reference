# PokéAPI: Get Language

Retrieves details for a language from PokéAPI.

```
GET https://connect.mindcloud.co/v1/universal/pokAPI/latest/actions/get-language
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a PokéAPI `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/pokAPI/latest/actions/get-language?connectionId=$CONNECTION_ID&languageId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "languageId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/pokAPI/latest/actions/get-language?${params}`, {
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
| `languageId` | string | yes | Identifier for the requested Language record. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "id": 1,
      "iso3166": "string",
      "iso639": "string",
      "name": "Ava Chen",
      "names": [
        {}
      ],
      "official": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `id` | number |  |
| `iso3166` | string |  |
| `iso639` | string |  |
| `name` | string |  |
| `names` | array<object> |  |
| `official` | boolean |  |

## Native endpoint

Through the native PokéAPI API, this operation is `GET language/:languageId` (base URL `https://pokeapi.co/api/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-language.md) for the provider-specific parameters and requirements.

