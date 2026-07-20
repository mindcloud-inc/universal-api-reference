# Powrbot: Search Company

Finds a company in Powrbot by company name.

```
GET https://connect.mindcloud.co/v1/universal/powrbot/latest/actions/search-company
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Powrbot `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/powrbot/latest/actions/search-company?connectionId=$CONNECTION_ID&company=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "company": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/powrbot/latest/actions/search-company?${params}`, {
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
| `company` | string | yes | Company name to search for. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "name": "Ava Chen",
      "search:display_url": "https://example.com",
      "search:snippet": "string",
      "wiki:Industry": [
        "string"
      ],
      "wiki:Website": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `name` | string |  |
| `search:display_url` | string |  |
| `search:snippet` | string |  |
| `wiki:Industry` | array<string> |  |
| `wiki:Website` | string |  |

## Native endpoint

Through the native Powrbot API, this operation is `GET /search/single/` (base URL `https://powrbot.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/search-company.md) for the provider-specific parameters and requirements.

