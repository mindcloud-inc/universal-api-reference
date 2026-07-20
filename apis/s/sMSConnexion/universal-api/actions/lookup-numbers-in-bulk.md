# SMS Connexion: Lookup Numbers In Bulk

Creates a bulk number lookup in SMS Connexion.

```
POST https://connect.mindcloud.co/v1/universal/sMSConnexion/latest/actions/lookup-numbers-in-bulk
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a SMS Connexion `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/sMSConnexion/latest/actions/lookup-numbers-in-bulk" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "phoneNumbers": {}
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/sMSConnexion/latest/actions/lookup-numbers-in-bulk', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "phoneNumbers": {}
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `phoneNumbers` | object<string> | yes | E.164 phone numbers to lookup in bulk. |
| `allowInvalid` | boolean | no | Allow invalid numbers instead of hard validation failure. |
| `countryIso` | string | no | ISO 3166-1 alpha-2 country used for number validation. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "cost": 1,
      "countryIso": "string",
      "data": [
        "string"
      ],
      "datetime": "string",
      "info": {},
      "invalid": [
        "string"
      ],
      "lookupBulkId": "string",
      "lookupId": "string",
      "phoneNumber": "string",
      "phoneNumbersByCountry": {},
      "totalCost": 1,
      "totalInvalid": 1,
      "totalPhoneNumbers": 1,
      "totalValid": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `cost` | number |  |
| `countryIso` | string |  |
| `data` | array |  |
| `datetime` | string |  |
| `info` | object |  |
| `invalid` | array |  |
| `lookupBulkId` | string |  |
| `lookupId` | string |  |
| `phoneNumber` | string |  |
| `phoneNumbersByCountry` | object |  |
| `totalCost` | number |  |
| `totalInvalid` | number |  |
| `totalPhoneNumbers` | number |  |
| `totalValid` | number |  |

## Native endpoint

Through the native SMS Connexion API, this operation is `POST /numbers/lookup` (base URL `https://api.sms.cx`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/lookup-numbers-in-bulk.md) for the provider-specific parameters and requirements.

