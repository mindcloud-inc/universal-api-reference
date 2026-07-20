# Salesrobot: Get Stats Range



```
GET https://connect.mindcloud.co/v1/universal/salesrobot/latest/actions/get-stats-range
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Salesrobot `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/salesrobot/latest/actions/get-stats-range?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/salesrobot/latest/actions/get-stats-range?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```



## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Salesrobot API returns.

## Native endpoint

Through the native Salesrobot API, this operation is `POST /api/campaign/stats` (base URL `https://api.boomtechinc.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-stats-range.md) for the provider-specific parameters and requirements.

