# ContactOut: Search People By Company

Finds people in ContactOut by company.

```
GET https://connect.mindcloud.co/v1/universal/contactOut/latest/actions/search-people-by-company
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ContactOut `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/contactOut/latest/actions/search-people-by-company?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/contactOut/latest/actions/search-people-by-company?${params}`, {
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
| `company` | string | no | Company name to search people within. |
| `page` | string | no | Results page number. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "message": "string",
      "metadata": {},
      "profiles": {},
      "status_code": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `message` | string | API response message. |
| `metadata` | object | Paging and result metadata. |
| `profiles` | object | Map of LinkedIn profile URLs to people search results for the requested company. |
| `status_code` | number | HTTP-style status code returned by ContactOut. |

## Native endpoint

Through the native ContactOut API, this operation is `POST /v1/people/search` (base URL `https://api.contactout.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/search-people-by-company.md) for the provider-specific parameters and requirements.

