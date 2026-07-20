# OpenThesaurus: Search Synonyms



```
GET https://connect.mindcloud.co/v1/universal/openThesaurus/latest/actions/search-synonyms
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a OpenThesaurus `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/openThesaurus/latest/actions/search-synonyms?connectionId=$CONNECTION_ID&q=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "q": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/openThesaurus/latest/actions/search-synonyms?${params}`, {
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
| `q` | string | yes |  |
| `similar` | boolean | no | Default: `false`. |
| `substring` | boolean | no | Default: `false`. |
| `startswith` | boolean | no | Default: `false`. |
| `supersynsets` | boolean | no | Default: `false`. |
| `subsynsets` | boolean | no | Default: `false`. |
| `baseform` | boolean | no | Default: `false`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "id": 1,
      "terms": [
        {
          "level": "string",
          "term": "string"
        }
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `id` | number | Synset identifier. |
| `terms[].level` | string | Term register or usage level when present. |
| `terms[].term` | string | Synonym term. |

## Native endpoint

Through the native OpenThesaurus API, this operation is `GET /` (base URL `https://www.openthesaurus.de/synonyme/search`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/search-synonyms.md) for the provider-specific parameters and requirements.

