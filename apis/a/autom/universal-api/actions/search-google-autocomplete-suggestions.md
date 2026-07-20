# Autom: Search Google Autocomplete Suggestions

Finds Google autocomplete suggestions in Autom.

```
GET https://connect.mindcloud.co/v1/universal/autom/latest/actions/search-google-autocomplete-suggestions
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Autom `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/autom/latest/actions/search-google-autocomplete-suggestions?connectionId=$CONNECTION_ID&query=MindCloud" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "query": "MindCloud"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/autom/latest/actions/search-google-autocomplete-suggestions?${params}`, {
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
| `query` | string | yes | The query to get autocomplete suggestions for. Example: `MindCloud`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "searchParameters": {
        "cp": 1,
        "engine": "string",
        "gl": "string",
        "googleDomain": "string",
        "hl": "string",
        "q": "string"
      },
      "suggestions": [
        {
          "value": "string"
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
| `searchParameters.cp` | number |  |
| `searchParameters.engine` | string |  |
| `searchParameters.gl` | string |  |
| `searchParameters.googleDomain` | string |  |
| `searchParameters.hl` | string |  |
| `searchParameters.q` | string |  |
| `suggestions[].value` | string |  |

## Native endpoint

Through the native Autom API, this operation is `GET /v1/google/search/autocomplete` (base URL `https://api.autom.dev`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/search-google-autocomplete-suggestions.md) for the provider-specific parameters and requirements.

