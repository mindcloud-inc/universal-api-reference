# ADP: Get Worker Pay Statement



```
GET https://connect.mindcloud.co/v1/universal/adp/latest/actions/list-worker-pay-statement-by-uri
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ADP `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/adp/latest/actions/list-worker-pay-statement-by-uri?connectionId=$CONNECTION_ID&aoid=string&payStatementId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "aoid": "string",
  "payStatementId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/adp/latest/actions/list-worker-pay-statement-by-uri?${params}`, {
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
| `aoid` | string | yes | The ADP associate object identifier for the worker whose pay statement should be returned. |
| `payStatementId` | string | yes | The pay statement identifier returned by List Worker Pay Statements. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native ADP API returns.

## Native endpoint

Through the native ADP API, this operation is `GET payroll/v1/workers/:aoid/organizational-pay-statements/:payStatementId` (base URL `https://api.adp.com/`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-worker-pay-statement-by-uri.md) for the provider-specific parameters and requirements.

