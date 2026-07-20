# OpenPLZ: Full Text Search Germany



```
GET https://connect.mindcloud.co/v1/universal/openPLZ/latest/actions/full-text-search-germany
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a OpenPLZ `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/openPLZ/latest/actions/full-text-search-germany?connectionId=$CONNECTION_ID&limit=25&offset=0&searchTerm=Berlin%20Pariser%20Platz" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0',
  "searchTerm": "Berlin Pariser Platz"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/openPLZ/latest/actions/full-text-search-germany?${params}`, {
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
| `searchTerm` | string | yes | Street name, postal code, or locality text to search for in Germany. Default: `Berlin Pariser Platz`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "borough": "string",
      "federalState": {},
      "locality": "string",
      "municipality": {},
      "name": "Ava Chen",
      "postalCode": "string",
      "suburb": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `borough` | string |  |
| `federalState` | object |  |
| `locality` | string |  |
| `municipality` | object |  |
| `name` | string |  |
| `postalCode` | string |  |
| `suburb` | string |  |

## Native endpoint

Through the native OpenPLZ API, this operation is `GET /de/FullTextSearch` (base URL `https://openplzapi.org`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/full-text-search-germany.md) for the provider-specific parameters and requirements.

