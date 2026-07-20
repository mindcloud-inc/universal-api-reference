# Active Network: Search Campsites

Finds campsites in Active Network.

```
GET https://connect.mindcloud.co/v1/universal/activeNetwork/latest/actions/search-campsites
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Active Network `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/activeNetwork/latest/actions/search-campsites?connectionId=$CONNECTION_ID&contractCode=string&parkId=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "contractCode": "string",
  "parkId": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/activeNetwork/latest/actions/search-campsites?${params}`, {
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
| `contractCode` | string | yes | Jurisdiction code returned by campground search. |
| `equipmentLength` | number | no | Required equipment length for the campsite. |
| `hookup` | string | no | Electric hookup code. |
| `maxPeople` | string | no | Maximum number of campers the site must support. |
| `parkId` | number | yes | Unique campground facility ID returned by campground search. |
| `petsAllowed` | string | no | Pets-allowed code. |
| `pullThrough` | string | no | Pull-through driveway code. |
| `sewer` | string | no | Sewer hookup code. |
| `siteType` | number | no | Site type code such as RV, tent, trailer, or cabin. |
| `water` | string | no | Water hookup code. |
| `waterfront` | string | no | Waterfront-site code. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Active Network API returns.

## Native endpoint

Through the native Active Network API, this operation is `GET /camping/campsites/` (base URL `http://api.amp.active.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/search-campsites.md) for the provider-specific parameters and requirements.

