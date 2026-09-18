# Paycom: Get Employee Effective Rate



```
GET https://connect.mindcloud.co/v1/universal/paycom/latest/actions/get-employee-effective-rate
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Paycom `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/paycom/latest/actions/get-employee-effective-rate?connectionId=$CONNECTION_ID&eecode=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "eecode": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/paycom/latest/actions/get-employee-effective-rate?${params}`, {
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
| `eecode` | string | yes |  |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Paycom API returns.

## Native endpoint

Through the native Paycom API, this operation is `GET api/v1/employee/:eecode/effectiveratesbyallocation` (base URL `https://api.paycomonline.net/v4/rest/index.php/`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-employee-effective-rate.md) for the provider-specific parameters and requirements.

