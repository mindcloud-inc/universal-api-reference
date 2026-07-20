# SMS Connexion: Get Number Lookup Status

Retrieves a number lookup result from SMS Connexion.

```
GET https://connect.mindcloud.co/v1/universal/sMSConnexion/latest/actions/get-number-lookup-status
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a SMS Connexion `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/sMSConnexion/latest/actions/get-number-lookup-status?connectionId=$CONNECTION_ID&lookupId=f4d41f5b-7421-4d84-97dc-7fcb1b27d264" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "lookupId": "f4d41f5b-7421-4d84-97dc-7fcb1b27d264"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/sMSConnexion/latest/actions/get-number-lookup-status?${params}`, {
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
| `lookupId` | string | yes | Lookup UUID. Example: `f4d41f5b-7421-4d84-97dc-7fcb1b27d264`. |

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

Through the native SMS Connexion API, this operation is `GET /numbers/lookup/lookupId/:lookupId` (base URL `https://api.sms.cx`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-number-lookup-status.md) for the provider-specific parameters and requirements.

