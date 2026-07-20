# LEADTEX: Add Funds To Contact Account

Updates a contact account balance in LEADTEX by adding funds.

```
PUT https://connect.mindcloud.co/v1/universal/lEADTEX/latest/actions/add-funds-to-contact-account
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a LEADTEX `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/lEADTEX/latest/actions/add-funds-to-contact-account" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "account_id": 1,
  "amount": 1,
  "description": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/lEADTEX/latest/actions/add-funds-to-contact-account', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "account_id": 1,
    "amount": 1,
    "description": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `account_id` | number | yes | ID of the account to credit. |
| `amount` | number | yes | Amount in the smallest currency unit. |
| `description` | string | yes | Transaction description. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "data": {
        "amount": 1,
        "amount_note": "string",
        "created_at": "2026-05-07T12:00:00.000Z",
        "currency": "string",
        "id": 1,
        "updated_at": "2026-05-07T12:00:00.000Z"
      },
      "errors": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data` | object |  |
| `data.amount` | number |  |
| `data.amount_note` | string |  |
| `data.created_at` | date |  |
| `data.currency` | string |  |
| `data.id` | number |  |
| `data.updated_at` | date |  |
| `errors` | object |  |

## Native endpoint

Through the native LEADTEX API, this operation is `POST /addFundsToContactAccount?api_token={{credentials.apiKey}}` (base URL `https://app.leadteh.ru/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/add-funds-to-contact-account.md) for the provider-specific parameters and requirements.

