# Watbot: Add Funds To Contact Account

Adds funds to a contact account in Watbot.

```
PUT https://connect.mindcloud.co/v1/universal/watbot/latest/actions/add-funds-to-contact-account
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Watbot `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/watbot/latest/actions/add-funds-to-contact-account" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "accountId": "6",
  "amount": "100",
  "description": "Stage 3 funding"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/watbot/latest/actions/add-funds-to-contact-account', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "accountId": "6",
    "amount": "100",
    "description": "Stage 3 funding"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `accountId` | number | yes | ID of the contact account. Example: `6`. |
| `amount` | number | yes | Amount in the minor currency unit. Example: `100`. |
| `description` | string | yes | Transaction description. Example: `Stage 3 funding`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "amount": 1,
      "amountNote": "string",
      "createdAt": "2026-05-07T12:00:00.000Z",
      "currency": "string",
      "id": 1,
      "updatedAt": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `amount` | number | Balance in the minor currency unit. |
| `amountNote` | string | Human-readable balance display. |
| `createdAt` | date | Account creation timestamp. |
| `currency` | string | Three-letter ISO 4217 currency code. |
| `id` | number | Account ID. |
| `updatedAt` | date | Account update timestamp. |

## Native endpoint

Through the native Watbot API, this operation is `POST /addFundsToContactAccount` (base URL `https://watbot.ru/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/add-funds-to-contact-account.md) for the provider-specific parameters and requirements.

