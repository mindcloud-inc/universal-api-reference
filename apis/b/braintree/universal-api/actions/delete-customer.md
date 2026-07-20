# Braintree: Delete Customer

Deletes an existing customer from Braintree.

```
DELETE https://connect.mindcloud.co/v1/universal/braintree/latest/actions/delete-customer
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Braintree `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/braintree/latest/actions/delete-customer?connectionId=$CONNECTION_ID&customerId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "customerId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/braintree/latest/actions/delete-customer?${params}`, {
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
| `customerId` | string | yes | The GraphQL ID of the customer to delete. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "clientMutationId": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `clientMutationId` | string | Mutation correlation ID returned by Braintree. |

## Native endpoint

Through the native Braintree API, this operation is `POST /graphql` (base URL `https://payments.sandbox.braintree-api.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-customer.md) for the provider-specific parameters and requirements.

