# Fiserv: Search Payment Intents

Finds payment intents in Fiserv by filter criteria.

```
GET https://connect.mindcloud.co/v1/universal/fiserv/latest/actions/search-payment-intents
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Fiserv `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/fiserv/latest/actions/search-payment-intents?connectionId=$CONNECTION_ID&xAccountId=string&requestBody=%5Bobject%20Object%5D" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "xAccountId": "string",
  "requestBody": "[object Object]"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/fiserv/latest/actions/search-payment-intents?${params}`, {
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
| `requestBody` | object | yes | JSON request body from the official payment intent search schema. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Fiserv API returns.

## Native endpoint

Through the native Fiserv API, this operation is `POST /payment_intents/search` (base URL `https://bankinghub-cert.fiservapis.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/search-payment-intents.md) for the provider-specific parameters and requirements.

