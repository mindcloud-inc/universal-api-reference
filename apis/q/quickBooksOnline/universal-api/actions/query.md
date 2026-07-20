# QuickBooks Online: Query



```
GET https://connect.mindcloud.co/v1/universal/quickBooksOnline/latest/actions/query
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a QuickBooks Online `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/quickBooksOnline/latest/actions/query?connectionId=$CONNECTION_ID&query=select%20*%20from%20Customer" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "query": "select * from Customer"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/quickBooksOnline/latest/actions/query?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as query string parameters ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `query` | string | yes | QuickBooks SQL-like query string, for example select * from Customer. Example: `select * from Customer`. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native QuickBooks Online API returns.

## Native endpoint

Through the native QuickBooks Online API, this operation is `GET /query` (base URL `https://:quickbooksEnvironment/v3/company/:realmId`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/query.md) for the provider-specific parameters and requirements.

