# Twig Business: List Data Sources



```
GET https://connect.mindcloud.co/v1/universal/twigBusiness/latest/actions/list-data-sources
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Twig Business `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/twigBusiness/latest/actions/list-data-sources?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/twigBusiness/latest/actions/list-data-sources?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```



## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Twig Business API returns.

## Native endpoint

Through the native Twig Business API, this operation is `GET data-specs` (base URL `https://app.twig.so/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-data-sources.md) for the provider-specific parameters and requirements.

