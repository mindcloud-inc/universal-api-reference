# Active Network: Search Assets

Finds activity assets in Active Network.

```
GET https://connect.mindcloud.co/v1/universal/activeNetwork/latest/actions/search-assets
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Active Network `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`), [sorting](../sorting.md) (`sort`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/activeNetwork/latest/actions/search-assets?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/activeNetwork/latest/actions/search-assets?${params}`, {
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
| `category` | string | no | Restrict results to one ACTIVE category. |
| `latLon` | string | no | Latitude and longitude separated by a comma. |
| `near` | string | no | Place name to geocode, such as City, State, Country. |
| `query` | string | no | Keywords to search across ACTIVE assets. |
| `radius` | number | no | Search radius around the provided near or lat/lon location. |
| `startDate` | string | no | Start-date range in yyyy-mm-dd..yyyy-mm-dd format. |
| `topicName` | string | no | Restrict results to one or more topic names. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Active Network API returns.

## Native endpoint

Through the native Active Network API, this operation is `GET /v2/search` (base URL `http://api.amp.active.com`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/search-assets.md) for the provider-specific parameters and requirements.

