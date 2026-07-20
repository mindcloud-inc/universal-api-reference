# ShinyStat: List Landing Pages

Retrieves landing page metrics from ShinyStat.

```
GET https://connect.mindcloud.co/v1/universal/shinyStat/latest/actions/list-landing-pages
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ShinyStat `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/shinyStat/latest/actions/list-landing-pages?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/shinyStat/latest/actions/list-landing-pages?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```



## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native ShinyStat API returns.

## Native endpoint

Through the native ShinyStat API, this operation is `GET /pages/enter` (base URL `https://report.shinystat.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-landing-pages.md) for the provider-specific parameters and requirements.

