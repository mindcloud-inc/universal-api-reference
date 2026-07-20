# HelpDocs: Get Top Articles

Retrieves top articles from HelpDocs.

```
GET https://connect.mindcloud.co/v1/universal/helpDocs/latest/actions/get-top-articles
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a HelpDocs `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/helpDocs/latest/actions/get-top-articles?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/helpDocs/latest/actions/get-top-articles?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```



## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native HelpDocs API returns.

## Native endpoint

Through the native HelpDocs API, this operation is `GET /stats/article` (base URL `https://api.helpdocs.io/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-top-articles.md) for the provider-specific parameters and requirements.

