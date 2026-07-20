# OpenPLZ: Full Text Search Switzerland



```
GET https://connect.mindcloud.co/v1/universal/openPLZ/latest/actions/full-text-search-switzerland
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a OpenPLZ `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/openPLZ/latest/actions/full-text-search-switzerland?connectionId=$CONNECTION_ID&limit=25&offset=0&searchTerm=5000%20Aarau" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0',
  "searchTerm": "5000 Aarau"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/openPLZ/latest/actions/full-text-search-switzerland?${params}`, {
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
| `searchTerm` | string | yes | Street name, postal code, or locality text to search for in Switzerland. Default: `5000 Aarau`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "canton": {},
      "commune": {},
      "district": {},
      "key": "string",
      "locality": "string",
      "name": "Ava Chen",
      "postalCode": "string",
      "status": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `canton` | object |  |
| `commune` | object |  |
| `district` | object |  |
| `key` | string |  |
| `locality` | string |  |
| `name` | string |  |
| `postalCode` | string |  |
| `status` | string |  |

## Native endpoint

Through the native OpenPLZ API, this operation is `GET /ch/FullTextSearch` (base URL `https://openplzapi.org`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/full-text-search-switzerland.md) for the provider-specific parameters and requirements.

