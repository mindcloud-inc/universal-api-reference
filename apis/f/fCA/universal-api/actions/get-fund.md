# FCA: Get fund



```
GET https://connect.mindcloud.co/v1/universal/fCA/latest/actions/get-fund
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a FCA `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/fCA/latest/actions/get-fund?connectionId=$CONNECTION_ID&prn=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "prn": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/fCA/latest/actions/get-fund?${params}`, {
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
| `prn` | string | yes | FCA product reference number for a fund or collective investment scheme. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native FCA API returns.

## Native endpoint

Through the native FCA API, this operation is `GET /CIS/:prn` (base URL `https://register.fca.org.uk/services/V0.1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-fund.md) for the provider-specific parameters and requirements.

