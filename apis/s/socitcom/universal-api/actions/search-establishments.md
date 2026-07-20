# Société.com: Search Establishments

Finds establishments in Société.com by company name.

```
GET https://connect.mindcloud.co/v1/universal/socitcom/latest/actions/search-establishments
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Société.com `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/socitcom/latest/actions/search-establishments?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/socitcom/latest/actions/search-establishments?${params}`, {
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
| `companyName` | string | no | Company name to search establishments for. |
| `limit` | string | no | Maximum results to return. |
| `start` | string | no | Result offset, starting at 1. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "nbtot": 1,
      "page": 1,
      "results": [
        {}
      ],
      "totalpages": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `nbtot` | number | Total matching establishments returned by the search. |
| `page` | number | Current result page returned by the establishment search. |
| `results` | array<object> | Matching establishment records returned by the search. |
| `totalpages` | number | Total available establishment result pages. |

## Native endpoint

Through the native Société.com API, this operation is `GET /etablissement/search` (base URL `https://api.societe.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/search-establishments.md) for the provider-specific parameters and requirements.

