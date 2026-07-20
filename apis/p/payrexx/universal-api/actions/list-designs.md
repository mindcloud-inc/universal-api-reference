# Payrexx: List Designs

Retrieves designs from Payrexx.

```
GET https://connect.mindcloud.co/v1/universal/payrexx/latest/actions/list-designs
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Payrexx `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/payrexx/latest/actions/list-designs?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/payrexx/latest/actions/list-designs?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```



## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Payrexx API returns.

## Native endpoint

Through the native Payrexx API, this operation is `GET Design/` (base URL `https://api.payrexx.com/v1.14/`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-designs.md) for the provider-specific parameters and requirements.

