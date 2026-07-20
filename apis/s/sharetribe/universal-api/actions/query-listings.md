# Sharetribe: Query Listings

Retrieves listings from Sharetribe.

```
GET https://connect.mindcloud.co/v1/universal/sharetribe/latest/actions/query-listings
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Sharetribe `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`), [sorting](../sorting.md) (`sort`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/sharetribe/latest/actions/query-listings?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/sharetribe/latest/actions/query-listings?${params}`, {
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
| `authorId` | string | no | Match only listings belonging to this user ID. |
| `ids` | string | no | Comma-separated list of listing IDs to match, up to 100 IDs. Accepts multiple values in one string, delimited by `,`. |
| `states` | string | no | Comma-separated list of listing states to include. Accepts multiple values in one string, delimited by `,`. |
| `createdAtStart` | date | no | Filter listings created on or after this ISO 8601 timestamp. |
| `createdAtEnd` | date | no | Filter listings created before this ISO 8601 timestamp. |
| `keywords` | string | no | Keywords to match against listing title, description, and eligible public data text fields. |
| `origin` | string | no | Origin coordinates as latitude,longitude. Cannot be combined with keywords. |
| `bounds` | string | no | Bounding box coordinates as NE lat,NE lng,SW lat,SW lng. |
| `price` | string | no | Price filter using minor units. Supports VALUE, START,END, START, or ,END syntax. |
| `start` | date | no | Availability interval start time in ISO 8601 format. |
| `end` | date | no | Availability interval end time in ISO 8601 format. |
| `seats` | number | no | Minimum number of available seats required for the interval. |
| `availability` | string | no | Availability search type: day-full, day-partial, time-full, or time-partial. |
| `minDuration` | number | no | Minimum matching availability duration within the requested range. |
| `stockMode` | string | no | Stock query mode: strict or match-undefined. |
| `minStock` | number | no | Match listings whose current stock quantity is at least this value. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "attributes": {},
      "id": "string",
      "relationships": {},
      "type": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `attributes` | object | Resource attributes payload. |
| `id` | string | Resource ID. |
| `relationships` | object | Resource relationships payload. |
| `type` | string | Resource type. |

## Native endpoint

Through the native Sharetribe API, this operation is `GET listings/query` (base URL `https://flex-integ-api.sharetribe.com/v1/integration_api`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/query-listings.md) for the provider-specific parameters and requirements.

