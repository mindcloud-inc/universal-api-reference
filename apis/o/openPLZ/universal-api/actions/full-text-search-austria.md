# OpenPLZ: Full Text Search Austria



```
GET https://connect.mindcloud.co/v1/universal/openPLZ/latest/actions/full-text-search-austria
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a OpenPLZ `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/openPLZ/latest/actions/full-text-search-austria?connectionId=$CONNECTION_ID&limit=25&offset=0&searchTerm=Wien%20Stephansplatz" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0',
  "searchTerm": "Wien Stephansplatz"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/openPLZ/latest/actions/full-text-search-austria?${params}`, {
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
| `searchTerm` | string | yes | Street name, postal code, or locality text to search for in Austria. Default: `Wien Stephansplatz`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "district": {},
      "federalProvince": {},
      "key": "string",
      "locality": "string",
      "municipality": {},
      "name": "Ava Chen",
      "postalCode": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `district` | object |  |
| `federalProvince` | object |  |
| `key` | string |  |
| `locality` | string |  |
| `municipality` | object |  |
| `name` | string |  |
| `postalCode` | string |  |

## Native endpoint

Through the native OpenPLZ API, this operation is `GET /at/FullTextSearch` (base URL `https://openplzapi.org`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/full-text-search-austria.md) for the provider-specific parameters and requirements.

