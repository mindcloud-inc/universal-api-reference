# Jobicy: List Education Remote Jobs



```
GET https://connect.mindcloud.co/v1/universal/jobicy/latest/actions/list-education-remote-jobs
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Jobicy `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/jobicy/latest/actions/list-education-remote-jobs?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/jobicy/latest/actions/list-education-remote-jobs?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```



## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Jobicy API returns.

## Native endpoint

Through the native Jobicy API, this operation is `GET /remote-jobs` (base URL `https://jobicy.com/api/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-education-remote-jobs.md) for the provider-specific parameters and requirements.

