# Financial Modeling Prep: Search Companies By Name

Finds companies in Financial Modeling Prep by name.

```
GET https://connect.mindcloud.co/v1/universal/financialModelingPrep/latest/actions/search-companies-by-name
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Financial Modeling Prep `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/financialModelingPrep/latest/actions/search-companies-by-name?connectionId=$CONNECTION_ID&query=Apple" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "query": "Apple"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/financialModelingPrep/latest/actions/search-companies-by-name?${params}`, {
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
| `query` | string | yes | Company or asset name to search for, such as Apple. Example: `Apple`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "currency": "string",
      "exchange": "string",
      "exchangeFullName": "Ava Chen",
      "name": "Ava Chen",
      "symbol": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `currency` | string |  |
| `exchange` | string |  |
| `exchangeFullName` | string |  |
| `name` | string |  |
| `symbol` | string |  |

## Native endpoint

Through the native Financial Modeling Prep API, this operation is `GET /search-name` (base URL `https://financialmodelingprep.com/stable`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/search-companies-by-name.md) for the provider-specific parameters and requirements.

