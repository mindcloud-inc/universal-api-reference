# Paycom: List Employees Active



```
GET https://connect.mindcloud.co/v1/universal/paycom/latest/actions/list-employees-active
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Paycom `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/paycom/latest/actions/list-employees-active?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/paycom/latest/actions/list-employees-active?${params}`, {
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
| `pagesize` | number | no | Default: `500`. |
| `eestatus` | string | no | Default: `A`. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Paycom API returns.

## Native endpoint

Through the native Paycom API, this operation is `GET api/v1/employeeid` (base URL `https://api.paycomonline.net/v4/rest/index.php/`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-employees-active.md) for the provider-specific parameters and requirements.

