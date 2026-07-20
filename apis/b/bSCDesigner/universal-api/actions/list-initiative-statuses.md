# BSC Designer: List Initiative Statuses



```
GET https://connect.mindcloud.co/v1/universal/bSCDesigner/latest/actions/list-initiative-statuses
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a BSC Designer `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/bSCDesigner/latest/actions/list-initiative-statuses?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/bSCDesigner/latest/actions/list-initiative-statuses?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```



## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native BSC Designer API returns.

## Native endpoint

Through the native BSC Designer API, this operation is `GET /rest/api/initiative-statuses` (base URL `https://www.webbsc.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-initiative-statuses.md) for the provider-specific parameters and requirements.

