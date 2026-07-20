# Get Website Report: List User Reports



```
GET https://connect.mindcloud.co/v1/universal/getWebsiteReport/latest/actions/list-user-reports
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Get Website Report `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/getWebsiteReport/latest/actions/list-user-reports?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/getWebsiteReport/latest/actions/list-user-reports?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```



## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Get Website Report API returns.

## Native endpoint

Through the native Get Website Report API, this operation is `GET /user_reports` (base URL `https://gwr-v3-prod-dot-turing-alcove-395007.el.r.appspot.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-user-reports.md) for the provider-specific parameters and requirements.

