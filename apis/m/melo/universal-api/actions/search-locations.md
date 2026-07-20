# Melo: Search Locations

Finds locations in Melo by search term.

```
GET https://connect.mindcloud.co/v1/universal/melo/latest/actions/search-locations
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Melo `connectionId` ([setup](../authentication.md)).

This action also supports [filtering](../filtering.md) (`where`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/melo/latest/actions/search-locations?connectionId=$CONNECTION_ID&query=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "query": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/melo/latest/actions/search-locations?${params}`, {
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
| `query` | string | yes | Search text for location suggestions. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "code": "string",
      "displayName": "Ava Chen",
      "groupedCityNames": [
        "Ava Chen"
      ],
      "name": "Ava Chen",
      "zipcode": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `code` | string |  |
| `displayName` | string |  |
| `groupedCityNames[]` | string |  |
| `name` | string |  |
| `zipcode` | string |  |

## Native endpoint

Through the native Melo API, this operation is `GET /public/location-autocomplete` (base URL `https://preprod-api.notif.immo`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/search-locations.md) for the provider-specific parameters and requirements.

