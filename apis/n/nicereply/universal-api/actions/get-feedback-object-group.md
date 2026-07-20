# Nicereply: Get Feedback Object Group

Retrieves a feedback object group from Nicereply.

```
GET https://connect.mindcloud.co/v1/universal/nicereply/latest/actions/get-feedback-object-group
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Nicereply `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/nicereply/latest/actions/get-feedback-object-group?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/nicereply/latest/actions/get-feedback-object-group?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```



## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Nicereply API returns.

## Native endpoint

Through the native Nicereply API, this operation is `GET /feedback-object-groups/:id` (base URL `https://api.nicereply.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-feedback-object-group.md) for the provider-specific parameters and requirements.

