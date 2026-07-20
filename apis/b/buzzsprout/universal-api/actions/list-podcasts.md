# Buzzsprout: List Podcasts

Retrieves podcasts from Buzzsprout.

```
GET https://connect.mindcloud.co/v1/universal/buzzsprout/latest/actions/list-podcasts
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Buzzsprout `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/buzzsprout/latest/actions/list-podcasts?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/buzzsprout/latest/actions/list-podcasts?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```



## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Buzzsprout API returns.

## Native endpoint

Through the native Buzzsprout API, this operation is `GET /podcasts.json` (base URL `https://www.buzzsprout.com/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-podcasts.md) for the provider-specific parameters and requirements.

