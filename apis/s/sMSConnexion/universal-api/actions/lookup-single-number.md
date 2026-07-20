# SMS Connexion: Lookup Single Number

Looks up a phone number in SMS Connexion.

```
GET https://connect.mindcloud.co/v1/universal/sMSConnexion/latest/actions/lookup-single-number
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a SMS Connexion `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/sMSConnexion/latest/actions/lookup-single-number?connectionId=$CONNECTION_ID&phoneNumber=%2B33612246450" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "phoneNumber": "+33612246450"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/sMSConnexion/latest/actions/lookup-single-number?${params}`, {
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
| `phoneNumber` | string | yes | Phone number in E.164 format, e.g. +33612246450. Example: `+33612246450`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "cost": 1,
      "countryIso": "string",
      "countryName": "Ava Chen",
      "countryNameLocale": "Ava Chen",
      "data": {},
      "datetime": "string",
      "lookupId": "string",
      "mcc": "string",
      "mccmnc": "string",
      "mnc": "string",
      "name": "Ava Chen",
      "originalNetwork": {},
      "phoneNumber": "string",
      "ported": true,
      "portedNetwork": {},
      "roaming": true,
      "roamingNetwork": {},
      "status": "string",
      "statusDescription": "string"
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
| `countryName` | string |  |
| `countryNameLocale` | string |  |
| `data` | object |  |
| `datetime` | string |  |
| `lookupId` | string |  |
| `mcc` | string |  |
| `mccmnc` | string |  |
| `mnc` | string |  |
| `name` | string |  |
| `originalNetwork` | object |  |
| `phoneNumber` | string |  |
| `ported` | boolean |  |
| `portedNetwork` | object |  |
| `roaming` | boolean |  |
| `roamingNetwork` | object |  |
| `status` | string |  |
| `statusDescription` | string |  |

## Native endpoint

Through the native SMS Connexion API, this operation is `GET /numbers/lookup/:phoneNumber` (base URL `https://api.sms.cx`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/lookup-single-number.md) for the provider-specific parameters and requirements.

