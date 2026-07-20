# AppFollow: Get Ratings History

Retrieves ratings history from AppFollow.

```
GET https://connect.mindcloud.co/v1/universal/appFollow/latest/actions/get-ratings-history
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a AppFollow `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/appFollow/latest/actions/get-ratings-history?connectionId=$CONNECTION_ID&store=string&collectionName=Ava%20Chen&extId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "store": "string",
  "collectionName": "Ava Chen",
  "extId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/appFollow/latest/actions/get-ratings-history?${params}`, {
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
| `country` | string | no | Country code. |
| `countries` | string | no | Country code list. |
| `from` | string | no | Start date. |
| `to` | string | no | End date. |
| `period` | string | no | Aggregation period. |
| `store` | string | yes | Store identifier. |
| `collectionName` | string | yes | Collection name. |
| `extId` | string | yes | App external ID. |
| `includeNegativeChanges` | boolean | no | Include negative changes. |
| `type` | string | no | Metric type. |
| `offset` | number | no | Offset. |
| `limit` | number | no | Limit. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native AppFollow API returns.

## Native endpoint

Through the native AppFollow API, this operation is `GET /api/v2/meta/ratings/history` (base URL `https://api.appfollow.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-ratings-history.md) for the provider-specific parameters and requirements.

