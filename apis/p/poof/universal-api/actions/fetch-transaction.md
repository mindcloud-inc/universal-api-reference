# Poof: Fetch Transaction

Retrieves a transaction record from Poof.

```
GET https://connect.mindcloud.co/v1/universal/poof/latest/actions/fetch-transaction
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Poof `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/poof/latest/actions/fetch-transaction?connectionId=$CONNECTION_ID&transaction=13f5d844" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "transaction": "13f5d844"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/poof/latest/actions/fetch-transaction?${params}`, {
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
| `transaction` | string | yes | Transaction identifier. Default: `13f5d844`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "amount": "string",
      "currency": "string",
      "date": "string",
      "email": "ava@example.com",
      "items": "string",
      "metadata": {},
      "name": "Ava Chen",
      "note": "string",
      "paid": "string",
      "paymentId": "string",
      "paymentMethod": "string",
      "quantities": "string",
      "streetAddress": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `amount` | string |  |
| `currency` | string |  |
| `date` | string |  |
| `email` | string |  |
| `items` | string |  |
| `metadata` | object |  |
| `name` | string |  |
| `note` | string |  |
| `paid` | string |  |
| `paymentId` | string |  |
| `paymentMethod` | string |  |
| `quantities` | string |  |
| `streetAddress` | string |  |

## Native endpoint

Through the native Poof API, this operation is `POST https://www.poof.io/api/v1/transaction` (base URL `https://www.poof.io/api/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/fetch-transaction.md) for the provider-specific parameters and requirements.

