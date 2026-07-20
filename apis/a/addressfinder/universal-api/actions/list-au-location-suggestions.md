# Addressfinder: List AU Location Suggestions

Finds Australian location suggestions in Addressfinder by partial query.

```
GET https://connect.mindcloud.co/v1/universal/addressfinder/latest/actions/list-au-location-suggestions
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Addressfinder `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/addressfinder/latest/actions/list-au-location-suggestions?connectionId=$CONNECTION_ID&q=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "q": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/addressfinder/latest/actions/list-au-location-suggestions?${params}`, {
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
| `q` | string | yes | The query string to match against locations. |
| `locationTypes` | string | no | Comma-separated location types to allow: street, locality, or state. |
| `stateCodes` | string | no | Filter results by state or territory codes. |
| `domain` | string | no | Registered domain used for activity monitoring. |
| `max` | number | no | Maximum number of results to return. Default: `10`. |
| `highlight` | number | no | Set to 1 to include highlighted matching terms in the response. |
| `format` | string | no | Response format. Default: `json`. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Addressfinder API returns.

## Native endpoint

Through the native Addressfinder API, this operation is `GET /au/location/autocomplete` (base URL `https://api.addressfinder.io/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-au-location-suggestions.md) for the provider-specific parameters and requirements.

