# Poof: Create ACH Debit

Creates a new ACH debit in Poof.

```
POST https://connect.mindcloud.co/v1/universal/poof/latest/actions/create-ach-debit
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Poof `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/poof/latest/actions/create-ach-debit" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "amount": "1",
  "account_number": "000123456789",
  "routing_number": "110000000"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/poof/latest/actions/create-ach-debit', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "amount": "1",
    "account_number": "000123456789",
    "routing_number": "110000000"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `amount` | number | yes | ACH debit amount in USD. Default: `1`. |
| `account_number` | string | yes | Bank account number. Default: `000123456789`. |
| `routing_number` | string | yes | Bank routing number. Default: `110000000`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "response": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `response` | string |  |

## Native endpoint

Through the native Poof API, this operation is `POST https://www.poof.io/api/v2/ach_debit` (base URL `https://www.poof.io/api/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-ach-debit.md) for the provider-specific parameters and requirements.

