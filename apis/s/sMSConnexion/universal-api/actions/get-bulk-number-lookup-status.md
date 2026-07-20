# SMS Connexion: Get Bulk Number Lookup Status

Retrieves a bulk number lookup result from SMS Connexion.

```
GET https://connect.mindcloud.co/v1/universal/sMSConnexion/latest/actions/get-bulk-number-lookup-status
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a SMS Connexion `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/sMSConnexion/latest/actions/get-bulk-number-lookup-status?connectionId=$CONNECTION_ID&lookupBulkId=2fb73a52-38f8-4b45-ae4d-66de84d5e48e" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "lookupBulkId": "2fb73a52-38f8-4b45-ae4d-66de84d5e48e"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/sMSConnexion/latest/actions/get-bulk-number-lookup-status?${params}`, {
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
| `lookupBulkId` | string | yes | Bulk lookup UUID. Example: `2fb73a52-38f8-4b45-ae4d-66de84d5e48e`. |

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
      "data": [
        "string"
      ],
      "datetime": "string",
      "info": {},
      "lookupBulkId": "string",
      "lookupId": "string",
      "mcc": "string",
      "mccmnc": "string",
      "mnc": "string",
      "name": "Ava Chen",
      "originalNetwork": {},
      "phoneNumber": "string",
      "phoneNumbersByCountry": {},
      "ported": true,
      "portedNetwork": {},
      "roaming": true,
      "roamingNetwork": {},
      "status": "string",
      "statusDescription": "string",
      "totalCost": 1,
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
| `countryName` | string |  |
| `countryNameLocale` | string |  |
| `data` | array |  |
| `datetime` | string |  |
| `info` | object |  |
| `lookupBulkId` | string |  |
| `lookupId` | string |  |
| `mcc` | string |  |
| `mccmnc` | string |  |
| `mnc` | string |  |
| `name` | string |  |
| `originalNetwork` | object |  |
| `phoneNumber` | string |  |
| `phoneNumbersByCountry` | object |  |
| `ported` | boolean |  |
| `portedNetwork` | object |  |
| `roaming` | boolean |  |
| `roamingNetwork` | object |  |
| `status` | string |  |
| `statusDescription` | string |  |
| `totalCost` | number |  |
| `totalPhoneNumbers` | number |  |
| `totalValid` | number |  |

## Native endpoint

Through the native SMS Connexion API, this operation is `GET /numbers/lookup/lookupBulkId/:lookupBulkId` (base URL `https://api.sms.cx`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-bulk-number-lookup-status.md) for the provider-specific parameters and requirements.

