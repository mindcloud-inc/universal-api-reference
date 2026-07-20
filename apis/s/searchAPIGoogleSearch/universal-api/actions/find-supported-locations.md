# SearchAPI - Google Search: Find Supported Locations

Finds supported Google search locations in SearchAPI.

```
GET https://connect.mindcloud.co/v1/universal/searchAPIGoogleSearch/latest/actions/find-supported-locations
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a SearchAPI - Google Search `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/searchAPIGoogleSearch/latest/actions/find-supported-locations?connectionId=$CONNECTION_ID&q=london" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "q": "london"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/searchAPIGoogleSearch/latest/actions/find-supported-locations?${params}`, {
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
| `q` | string | yes | Location search text such as london or new york. Example: `london`. |
| `limit` | number | no | Maximum number of locations to return. Defaults to 10 and can be up to 100. Default: `10`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "canonical_name": "Ava Chen",
      "country_code": "string",
      "google_id": 1,
      "google_parent_id": 1,
      "lat": 1,
      "lon": 1,
      "name": "Ava Chen",
      "reach": 1,
      "target_type": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `canonical_name` | string | Canonical SearchAPI location name. |
| `country_code` | string | ISO country code. |
| `google_id` | number | Google location identifier. |
| `google_parent_id` | number | Google parent location identifier. |
| `lat` | number | Latitude. |
| `lon` | number | Longitude. |
| `name` | string | Location display name. |
| `reach` | number | Estimated location reach. |
| `target_type` | string | SearchAPI location target type. |

## Native endpoint

Through the native SearchAPI - Google Search API, this operation is `GET /locations` (base URL `https://www.searchapi.io/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/find-supported-locations.md) for the provider-specific parameters and requirements.

