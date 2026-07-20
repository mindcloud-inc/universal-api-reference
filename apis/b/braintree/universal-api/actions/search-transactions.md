# Braintree: Search Transactions

Finds transactions in Braintree by search criteria.

```
GET https://connect.mindcloud.co/v1/universal/braintree/latest/actions/search-transactions
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Braintree `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/braintree/latest/actions/search-transactions?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/braintree/latest/actions/search-transactions?${params}`, {
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
| `transactionIdIs` | string | no | Exact GraphQL transaction ID to search for. This filter does not accept the legacy transaction ID. |
| `statusIs` | string | no | Exact transaction status to search for. |

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

Through the native Braintree API, this operation is `POST /graphql` (base URL `https://payments.sandbox.braintree-api.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/search-transactions.md) for the provider-specific parameters and requirements.

