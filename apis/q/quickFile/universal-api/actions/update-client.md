# QuickFile: Update Client



```
PUT https://connect.mindcloud.co/v1/universal/quickFile/latest/actions/update-client
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a QuickFile `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/quickFile/latest/actions/update-client" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "clientId": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/quickFile/latest/actions/update-client', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "clientId": 1
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `clientId` | number | yes | QuickFile ClientID to update. |
| `companyName` | string | no | Updated client company or trading name. |
| `accountReference` | string | no | Updated external reference or short account code. |
| `city` | string | no | Updated town or city. |
| `addressLine1` | string | no | Updated first postal address line. |
| `postcode` | string | no | Updated postal or ZIP code. |
| `countryIso` | string | no | Updated two-letter ISO country code when supported. |
| `allowAttachPdf` | boolean | no | When true, keeps PDF email delivery enabled for this client. Default: `true`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "clientContactsUpdated": 1,
      "clientDetailsUpdated": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `clientContactsUpdated` | number | Count of contact rows updated by the request. |
| `clientDetailsUpdated` | boolean | Whether the supplier details payload was applied. |

## Native endpoint

Through the native QuickFile API, this operation is `POST /client/update` (base URL `https://api.quickfile.co.uk/1_2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-client.md) for the provider-specific parameters and requirements.

