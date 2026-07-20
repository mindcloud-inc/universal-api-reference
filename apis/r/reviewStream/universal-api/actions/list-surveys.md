# ReviewStream: List Surveys

Retrieves surveys from ReviewStream.

```
GET https://connect.mindcloud.co/v1/universal/reviewStream/latest/actions/list-surveys
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ReviewStream `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/reviewStream/latest/actions/list-surveys?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/reviewStream/latest/actions/list-surveys?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```



## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native ReviewStream API returns.

## Native endpoint

Through the native ReviewStream API, this operation is `GET /surveys` (base URL `https://api.reviewstream.ai/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-surveys.md) for the provider-specific parameters and requirements.

