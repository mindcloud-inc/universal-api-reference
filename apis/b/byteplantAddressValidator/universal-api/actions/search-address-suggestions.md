# Byteplant Address Validator: Search Address Suggestions

Finds address suggestions in Byteplant Address Validator.

```
GET https://connect.mindcloud.co/v1/universal/byteplantAddressValidator/latest/actions/search-address-suggestions
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Byteplant Address Validator `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/byteplantAddressValidator/latest/actions/search-address-suggestions?connectionId=$CONNECTION_ID&query=string&countryCode=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "query": "string",
  "countryCode": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/byteplantAddressValidator/latest/actions/search-address-suggestions?${params}`, {
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
| `query` | string | yes | Freeform address text to match against Byteplant suggestions. |
| `countryCode` | string | yes | Two-letter ISO 3166-1 country code. Use XX for international. |
| `matchLevel` | string | no | Optional suggestion granularity: locality, street, building, or subbuilding. |
| `locale` | string | no | Output language for countries with multiple postal languages. |
| `maxResults` | number | no | Maximum number of suggestions to return. Default: `5`. |
| `timeout` | number | no | Request timeout in seconds. Default: `10`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "description": "string",
      "id": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `description` | string | Human-readable address suggestion. |
| `id` | string | Suggestion identifier used by Get Address Details. |

## Native endpoint

Through the native Byteplant Address Validator API, this operation is `GET /api/search` (base URL `https://api.address-validator.net`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/search-address-suggestions.md) for the provider-specific parameters and requirements.

