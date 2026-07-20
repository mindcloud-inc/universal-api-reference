# Enrich.so: Suggest Company Names

Finds company name suggestions in Enrich.so.

```
GET https://connect.mindcloud.co/v1/universal/enrich/latest/actions/suggest-company-names
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Enrich.so `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/enrich/latest/actions/suggest-company-names?connectionId=$CONNECTION_ID&q=str" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "q": "str"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/enrich/latest/actions/suggest-company-names?${params}`, {
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
| `q` | string | yes | Company name prefix to suggest. Default: `str`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "domain": "string",
      "linkedinUrl": "https://example.com",
      "name": "Ava Chen"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `domain` | string | Company domain, when available. |
| `linkedinUrl` | string | Company LinkedIn URL, when available. |
| `name` | string | Suggested company name. |

## Native endpoint

Through the native Enrich.so API, this operation is `GET /lead-finder/suggest` (base URL `https://dev.enrich.so/api/v3`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/suggest-company-names.md) for the provider-specific parameters and requirements.

