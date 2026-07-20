# ContactOut: Search Companies HQ Only

Finds HQ-only companies in ContactOut using company search filters.

```
GET https://connect.mindcloud.co/v1/universal/contactOut/latest/actions/search-companies-hq-only
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ContactOut `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/contactOut/latest/actions/search-companies-hq-only?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/contactOut/latest/actions/search-companies-hq-only?${params}`, {
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
| `domain` | string | no | Company domain to search. |
| `name` | string | no | Company name to search. |
| `page` | string | no | Results page number. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "companies": [
        {}
      ],
      "message": "string",
      "metadata": {},
      "status_code": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `companies` | array<object> | Company search results limited to HQ matches. |
| `message` | string | API response message. |
| `metadata` | object | Paging and result metadata. |
| `status_code` | number | HTTP-style status code returned by ContactOut. |

## Native endpoint

Through the native ContactOut API, this operation is `POST /v1/company/search` (base URL `https://api.contactout.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/search-companies-hq-only.md) for the provider-specific parameters and requirements.

