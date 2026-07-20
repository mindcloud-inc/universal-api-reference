# Watbot: List Contact Accounts

Retrieves contact accounts from Watbot.

```
GET https://connect.mindcloud.co/v1/universal/watbot/latest/actions/list-contact-accounts
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Watbot `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/watbot/latest/actions/list-contact-accounts?connectionId=$CONNECTION_ID&contactId=123" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "contactId": "123"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/watbot/latest/actions/list-contact-accounts?${params}`, {
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
| `contactId` | number | yes | ID of an existing Watbot contact. Example: `123`. |

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

Through the native Watbot API, this operation is `GET /getContactAccounts` (base URL `https://watbot.ru/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-contact-accounts.md) for the provider-specific parameters and requirements.

