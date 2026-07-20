# Braintree: Find Transaction

Retrieves a transaction from Braintree by ID.

```
GET https://connect.mindcloud.co/v1/universal/braintree/latest/actions/find-transaction
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Braintree `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/braintree/latest/actions/find-transaction?connectionId=$CONNECTION_ID&transactionId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "transactionId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/braintree/latest/actions/find-transaction?${params}`, {
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
| `transactionId` | string | yes | The GraphQL ID of the transaction to fetch. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "amount": {},
      "createdAt": "string",
      "id": "string",
      "legacyId": "string",
      "status": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `amount` | object | Transaction amount payload. |
| `createdAt` | string |  |
| `id` | string |  |
| `legacyId` | string |  |
| `status` | string |  |

## Native endpoint

Through the native Braintree API, this operation is `POST /graphql` (base URL `https://payments.sandbox.braintree-api.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/find-transaction.md) for the provider-specific parameters and requirements.

