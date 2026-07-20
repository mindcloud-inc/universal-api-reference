# QuickFile: Get Client



```
GET https://connect.mindcloud.co/v1/universal/quickFile/latest/actions/get-client
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a QuickFile `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/quickFile/latest/actions/get-client?connectionId=$CONNECTION_ID&clientId=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "clientId": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/quickFile/latest/actions/get-client?${params}`, {
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
| `clientId` | number | yes | The QuickFile ClientID to retrieve. |
| `returnAddress` | boolean | no | When true, includes the client postal address. Default: `true`. |
| `returnVatDetails` | boolean | no | When true, includes VAT number and EC status. Default: `true`. |
| `returnPreferences` | boolean | no | When true, includes QuickFile client preferences. Default: `true`. |
| `returnClientContacts` | boolean | no | When true, includes associated client contacts. Default: `true`. |
| `returnFinancials` | boolean | no | When true, includes balances and credits on account. Default: `true`. |
| `returnGoCardlessDetails` | boolean | no | When true, includes GoCardless pre-auth details when available. Default: `false`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "balance": 1,
      "clientId": 1,
      "email": "ava@example.com",
      "name": "Ava Chen",
      "phone": "string",
      "vatNumber": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `balance` | number | Current client balance. |
| `clientId` | number | QuickFile client identifier. |
| `email` | string | Primary client email. |
| `name` | string | Client display name. |
| `phone` | string | Primary client phone number. |
| `vatNumber` | string | Client VAT number. |

## Native endpoint

Through the native QuickFile API, this operation is `POST /client/get` (base URL `https://api.quickfile.co.uk/1_2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-client.md) for the provider-specific parameters and requirements.

