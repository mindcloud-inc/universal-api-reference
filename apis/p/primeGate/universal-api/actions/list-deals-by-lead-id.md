# PrimeGate: List Deals by Lead ID



```
GET https://connect.mindcloud.co/v1/universal/primeGate/latest/actions/list-deals-by-lead-id
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a PrimeGate `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/primeGate/latest/actions/list-deals-by-lead-id?connectionId=$CONNECTION_ID&leadId=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "leadId": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/primeGate/latest/actions/list-deals-by-lead-id?${params}`, {
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
| `leadId` | number | yes |  |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native PrimeGate API returns.

## Native endpoint

Through the native PrimeGate API, this operation is `POST deal/get` (base URL `https://api.primegate.io/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-deals-by-lead-id.md) for the provider-specific parameters and requirements.

