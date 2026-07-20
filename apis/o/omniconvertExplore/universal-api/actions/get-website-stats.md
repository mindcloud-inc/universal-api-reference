# Omniconvert Explore: Get Website Stats

Retrieves website statistics from Omniconvert Explore.

```
GET https://connect.mindcloud.co/v1/universal/omniconvertExplore/latest/actions/get-website-stats
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Omniconvert Explore `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/omniconvertExplore/latest/actions/get-website-stats?connectionId=$CONNECTION_ID&websiteId=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "websiteId": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/omniconvertExplore/latest/actions/get-website-stats?${params}`, {
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
| `intervalEnd` | string | no | End date filter for the stats interval. |
| `intervalStart` | string | no | Start date filter for the stats interval. |
| `type` | string | no | Stats type selector documented by Omniconvert. |
| `websiteId` | number | yes | Website identifier used in the endpoint path. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Omniconvert Explore API returns.

## Native endpoint

Through the native Omniconvert Explore API, this operation is `GET /websites/:websiteId/stats` (base URL `https://api.omniconvert.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-website-stats.md) for the provider-specific parameters and requirements.

