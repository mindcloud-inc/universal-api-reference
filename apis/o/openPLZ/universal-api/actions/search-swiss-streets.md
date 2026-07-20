# OpenPLZ: Search Swiss Streets



```
GET https://connect.mindcloud.co/v1/universal/openPLZ/latest/actions/search-swiss-streets
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a OpenPLZ `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/openPLZ/latest/actions/search-swiss-streets?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/openPLZ/latest/actions/search-swiss-streets?${params}`, {
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
| `name` | string | no | Street name or POSIX regular expression pattern. |
| `postalCode` | string | no | Postal code or POSIX regular expression pattern. |
| `locality` | string | no | Locality name or POSIX regular expression pattern. |

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

Through the native OpenPLZ API, this operation is `GET /ch/Streets` (base URL `https://openplzapi.org`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/search-swiss-streets.md) for the provider-specific parameters and requirements.

