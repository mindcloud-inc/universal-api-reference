# Logo.dev: Search Company Domains

Finds company domains in Logo.dev.

```
GET https://connect.mindcloud.co/v1/universal/logodev/latest/actions/search-company-domains
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Logo.dev `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/logodev/latest/actions/search-company-domains?connectionId=$CONNECTION_ID&q=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "q": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/logodev/latest/actions/search-company-domains?${params}`, {
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
| `q` | string | yes | Brand name query. |
| `strategy` | string | no | Search strategy: typeahead or match. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "domain": "string",
      "logo_url": "https://example.com",
      "name": "Ava Chen"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `domain` | string |  |
| `logo_url` | string |  |
| `name` | string |  |

## Native endpoint

Through the native Logo.dev API, this operation is `GET /search` (base URL `https://api.logo.dev`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/search-company-domains.md) for the provider-specific parameters and requirements.

