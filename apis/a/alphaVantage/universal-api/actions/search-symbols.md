# Alpha Vantage: Search Symbols

Finds symbols in Alpha Vantage by keywords.

```
GET https://connect.mindcloud.co/v1/universal/alphaVantage/latest/actions/search-symbols
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Alpha Vantage `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/alphaVantage/latest/actions/search-symbols?connectionId=$CONNECTION_ID&keywords=e.g.%20tesco" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "keywords": "e.g. tesco"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/alphaVantage/latest/actions/search-symbols?${params}`, {
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
| `keywords` | string | yes | Query parameter $key for SYMBOL_SEARCH. Example: `e.g. tesco`. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `datatype` | string | no | Optional response format. Leave unset for JSON. One of: `0`, `1`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "Information": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `Information` | string |  |

## Native endpoint

Through the native Alpha Vantage API, this operation is `GET /query` (base URL `https://www.alphavantage.co`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/search-symbols.md) for the provider-specific parameters and requirements.

