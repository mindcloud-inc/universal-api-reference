# Alto: Filter Listings

Finds property listings in Alto by filter criteria.

```
GET https://connect.mindcloud.co/v1/universal/alto/latest/actions/filter-listings
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Alto `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`), [filtering](../filtering.md) (`where`), [sorting](../sorting.md) (`sort`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/alto/latest/actions/filter-listings?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/alto/latest/actions/filter-listings?${params}`, {
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
| `branchId` | string | no | Branch identifier filter. |
| `ownerId` | string | no | Owner contact identifier filter. |
| `status` | string | no | Listing status filter. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "bedrooms": 1,
      "branchId": "string",
      "createdDate": "2026-05-07T12:00:00.000Z",
      "modifiedDate": "2026-05-07T12:00:00.000Z",
      "price": 1,
      "propertyId": 1,
      "status": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `bedrooms` | number |  |
| `branchId` | string |  |
| `createdDate` | date |  |
| `modifiedDate` | date |  |
| `price` | number |  |
| `propertyId` | number |  |
| `status` | string |  |

## Native endpoint

Through the native Alto API, this operation is `GET /listing/filter` (base URL `https://api.alto.zoopladev.co.uk`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/filter-listings.md) for the provider-specific parameters and requirements.

