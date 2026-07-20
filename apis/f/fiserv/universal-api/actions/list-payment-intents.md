# Fiserv: List Payment Intents

Retrieves payment intents for an account from Fiserv.

```
GET https://connect.mindcloud.co/v1/universal/fiserv/latest/actions/list-payment-intents
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Fiserv `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/fiserv/latest/actions/list-payment-intents?connectionId=$CONNECTION_ID&limit=25&offset=0&xAccountId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0',
  "xAccountId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/fiserv/latest/actions/list-payment-intents?${params}`, {
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
| `xAccountId` | string | yes | Fiserv account id sent in the required x-account-id header. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Fiserv API returns.

## Native endpoint

Through the native Fiserv API, this operation is `GET /payment_intents` (base URL `https://bankinghub-cert.fiservapis.com`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-payment-intents.md) for the provider-specific parameters and requirements.

