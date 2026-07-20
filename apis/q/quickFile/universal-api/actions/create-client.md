# QuickFile: Create Client



```
POST https://connect.mindcloud.co/v1/universal/quickFile/latest/actions/create-client
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a QuickFile `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/quickFile/latest/actions/create-client" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "companyName": "Ava Chen"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/quickFile/latest/actions/create-client', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "companyName": "Ava Chen"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `companyName` | string | yes | Client company or trading name to create. |
| `accountReference` | string | no | Optional external reference or short account code for the client. |
| `city` | string | no | Town or city for the postal address. |
| `addressLine1` | string | no | First postal address line. |
| `postcode` | string | no | Postal or ZIP code. |
| `countryIso` | string | no | Two-letter ISO country code for the address when supported. |
| `allowAttachPdf` | boolean | no | When true, enables emailing PDF invoices to this client. Default: `true`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "clientContactIds": [
        1
      ],
      "clientId": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `clientContactIds` | array<number> | Any contact IDs created alongside the client. |
| `clientId` | number | QuickFile ClientID created by the request. |

## Native endpoint

Through the native QuickFile API, this operation is `POST /client/create` (base URL `https://api.quickfile.co.uk/1_2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-client.md) for the provider-specific parameters and requirements.

