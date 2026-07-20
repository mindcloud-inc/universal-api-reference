# Eduzz: Get Customer Details by Email

Retrieves customer details from Eduzz by email address.

```
GET https://connect.mindcloud.co/v1/universal/eduzz/latest/actions/get-customer-details-by-email
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Eduzz `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/eduzz/latest/actions/get-customer-details-by-email?connectionId=$CONNECTION_ID&email=buyer%40example.com" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "email": "buyer@example.com"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/eduzz/latest/actions/get-customer-details-by-email?${params}`, {
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
| `email` | string | yes | Customer email address. Example: `buyer@example.com`. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Eduzz API returns.

## Native endpoint

Through the native Eduzz API, this operation is `GET /myeduzz/v1/subscriptions/customers/:email` (base URL `https://api.eduzz.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-customer-details-by-email.md) for the provider-specific parameters and requirements.

