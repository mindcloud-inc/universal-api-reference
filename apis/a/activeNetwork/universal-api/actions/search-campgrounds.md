# Active Network: Search Campgrounds

Finds campgrounds in Active Network.

```
GET https://connect.mindcloud.co/v1/universal/activeNetwork/latest/actions/search-campgrounds
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Active Network `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/activeNetwork/latest/actions/search-campgrounds?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/activeNetwork/latest/actions/search-campgrounds?${params}`, {
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
| `amenity` | number | no | Campground amenity code such as fishing, hiking, or golf. |
| `equipmentLength` | number | no | Required equipment length for the campsite. |
| `hookup` | string | no | Electric hookup code. |
| `landmarkLatitude` | string | no | Latitude for fixed-point campground searches. |
| `landmarkLongitude` | string | no | Longitude for fixed-point campground searches. |
| `landmarkName` | string | no | Name label required with landmark latitude and longitude. |
| `maxPeople` | string | no | Maximum number of campers the site must support. |
| `parkName` | string | no | Return campgrounds whose names contain this text. |
| `petsAllowed` | string | no | Pets-allowed code. |
| `pullThrough` | string | no | Pull-through driveway code. |
| `sewer` | string | no | Sewer hookup code. |
| `siteType` | number | no | Site type code such as RV, tent, trailer, or cabin. |
| `stateProvince` | string | no | Two-character US state or Canadian province code. |
| `water` | string | no | Water hookup code. |
| `waterfront` | string | no | Waterfront-site code. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Active Network API returns.

## Native endpoint

Through the native Active Network API, this operation is `GET /camping/campgrounds/` (base URL `http://api.amp.active.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/search-campgrounds.md) for the provider-specific parameters and requirements.

