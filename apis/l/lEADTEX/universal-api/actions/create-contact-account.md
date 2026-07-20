# LEADTEX: Create Contact Account

Creates an ISO 4217 contact account in LEADTEX.

```
POST https://connect.mindcloud.co/v1/universal/lEADTEX/latest/actions/create-contact-account
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a LEADTEX `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/lEADTEX/latest/actions/create-contact-account" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "contact_id": 1,
  "currency": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/lEADTEX/latest/actions/create-contact-account', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "contact_id": 1,
    "currency": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `contact_id` | number | yes | ID of the contact to create the account for. |
| `currency` | string | yes | Three-letter ISO 4217 currency code, such as USD. |

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

Through the native LEADTEX API, this operation is `POST /addContactAccount?api_token={{credentials.apiKey}}` (base URL `https://app.leadteh.ru/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-contact-account.md) for the provider-specific parameters and requirements.

