# Salesrobot: List Campaign Prospects



```
GET https://connect.mindcloud.co/v1/universal/salesrobot/latest/actions/list-campaign-prospects
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Salesrobot `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`), [sorting](../sorting.md) (`sort`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/salesrobot/latest/actions/list-campaign-prospects?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/salesrobot/latest/actions/list-campaign-prospects?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```



## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Salesrobot API returns.

## Native endpoint

Through the native Salesrobot API, this operation is `GET /api/campaign/prospects` (base URL `https://api.boomtechinc.com`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-campaign-prospects.md) for the provider-specific parameters and requirements.

