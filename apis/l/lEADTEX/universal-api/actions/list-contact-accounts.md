# LEADTEX: List Contact Accounts

Retrieves ISO 4217 contact accounts from LEADTEX.

```
GET https://connect.mindcloud.co/v1/universal/lEADTEX/latest/actions/list-contact-accounts
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a LEADTEX `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/lEADTEX/latest/actions/list-contact-accounts?connectionId=$CONNECTION_ID&contact_id=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "contact_id": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/lEADTEX/latest/actions/list-contact-accounts?${params}`, {
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
| `contact_id` | number | yes | ID of the contact whose accounts should be returned. |

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
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data` | array<object> |  |
| `data.amount` | number |  |
| `data.amount_note` | string |  |
| `data.created_at` | date |  |
| `data.currency` | string |  |
| `data.id` | number |  |
| `data.updated_at` | date |  |

## Native endpoint

Through the native LEADTEX API, this operation is `GET /getContactAccounts?api_token={{credentials.apiKey}}` (base URL `https://app.leadteh.ru/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-contact-accounts.md) for the provider-specific parameters and requirements.

