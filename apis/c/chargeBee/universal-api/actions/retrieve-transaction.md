# ChargeBee: Retrieve Transaction

Retrieves a transaction from ChargeBee.

```
GET https://connect.mindcloud.co/v1/universal/chargeBee/latest/actions/retrieve-transaction
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ChargeBee `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/chargeBee/latest/actions/retrieve-transaction?connectionId=$CONNECTION_ID&transaction_id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "transaction_id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/chargeBee/latest/actions/retrieve-transaction?${params}`, {
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
| `transaction_id` | string | yes | The Chargebee transaction identifier. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "amount": 1,
      "customer_id": "string",
      "date": 1,
      "id": "string",
      "object": "string",
      "status": "string",
      "subscription_id": "string",
      "type": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `amount` | number |  |
| `customer_id` | string |  |
| `date` | number |  |
| `id` | string |  |
| `object` | string |  |
| `status` | string |  |
| `subscription_id` | string |  |
| `type` | string |  |

## Native endpoint

Through the native ChargeBee API, this operation is `GET transactions/:transaction_id` (base URL `https://{{credentials.baseUrl}}.chargebee.com/api/v2/`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/retrieve-transaction.md) for the provider-specific parameters and requirements.

