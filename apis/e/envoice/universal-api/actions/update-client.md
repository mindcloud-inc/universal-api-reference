# Envoice: Update Client

Updates an existing client in Envoice.

```
PUT https://connect.mindcloud.co/v1/universal/envoice/latest/actions/update-client
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Envoice `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/envoice/latest/actions/update-client" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "id": 1,
  "clientCurrencyId": 1,
  "clientCountryId": 1,
  "uiLanguageId": 1,
  "name": "Ava Chen",
  "email": "ava@example.com"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/envoice/latest/actions/update-client', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "id": 1,
    "clientCurrencyId": 1,
    "clientCountryId": 1,
    "uiLanguageId": 1,
    "name": "Ava Chen",
    "email": "ava@example.com"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `id` | number | yes | Client ID. |
| `clientCurrencyId` | number | yes | Currency ID for the client. |
| `clientCountryId` | number | yes | Country ID for the client. |
| `uiLanguageId` | number | yes | UI language ID for the client. |
| `name` | string | yes | Client display name. |
| `email` | string | yes | Primary client email address. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "Success": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `Success` | boolean | Whether the client update succeeded. |

## Native endpoint

Through the native Envoice API, this operation is `POST client/update` (base URL `https://www.envoice.in/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-client.md) for the provider-specific parameters and requirements.

