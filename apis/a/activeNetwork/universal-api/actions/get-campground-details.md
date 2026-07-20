# Active Network: Get Campground Details

Retrieves campground details in Active Network.

```
GET https://connect.mindcloud.co/v1/universal/activeNetwork/latest/actions/get-campground-details
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Active Network `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/activeNetwork/latest/actions/get-campground-details?connectionId=$CONNECTION_ID&contractCode=string&parkId=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "contractCode": "string",
  "parkId": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/activeNetwork/latest/actions/get-campground-details?${params}`, {
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
| `parkId` | number | yes | Unique campground facility ID returned by campground search. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Active Network API returns.

## Native endpoint

Through the native Active Network API, this operation is `GET /camping/campground/details` (base URL `http://api.amp.active.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-campground-details.md) for the provider-specific parameters and requirements.

