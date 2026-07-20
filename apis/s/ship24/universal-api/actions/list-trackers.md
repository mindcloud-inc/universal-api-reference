# Ship24: List Trackers

Retrieves existing shipment trackers from Ship24.

```
GET https://connect.mindcloud.co/v1/universal/ship24/latest/actions/list-trackers
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Ship24 `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/ship24/latest/actions/list-trackers?connectionId=$CONNECTION_ID&limit=25&offset=0&page=1&limit=100" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0',
  "page": "1",
  "limit": "100"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/ship24/latest/actions/list-trackers?${params}`, {
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
| `page` | number | yes | The page index, starting from 1. Default: `1`. Example: `1`. |
| `limit` | number | yes | The maximum number of trackers returned per page. Default: `100`. Example: `100`. |
| `sort` | number | no | Use 1 for oldest-first and -1 for newest-first by createdAt. One of: `0`, `1`. Default: `1`. Example: `-1`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "clientTrackerId": "string",
      "createdAt": "2026-05-07T12:00:00.000Z",
      "isSubscribed": true,
      "isTracked": true,
      "shipmentReference": "string",
      "trackerId": "string",
      "trackingNumber": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `clientTrackerId` | string | Client-defined tracker identifier. |
| `createdAt` | date | Tracker creation timestamp. |
| `isSubscribed` | boolean | Whether the tracker is active for webhook subscription. |
| `isTracked` | boolean | Whether Ship24 is still actively tracking this shipment. |
| `shipmentReference` | string | Shipment reference provided at tracker creation. |
| `trackerId` | string | Ship24 tracker identifier. |
| `trackingNumber` | string | Tracking number used for this tracker. |

## Native endpoint

Through the native Ship24 API, this operation is `GET /public/v1/trackers` (base URL `https://api.ship24.com`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-trackers.md) for the provider-specific parameters and requirements.

