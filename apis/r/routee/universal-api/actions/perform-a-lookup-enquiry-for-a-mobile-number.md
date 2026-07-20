# Routee: Perform a Lookup enquiry for a mobile number

Creates a number lookup request in Routee.

```
POST https://connect.mindcloud.co/v1/universal/routee/latest/actions/perform-a-lookup-enquiry-for-a-mobile-number
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Routee `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/routee/latest/actions/perform-a-lookup-enquiry-for-a-mobile-number" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "to": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/routee/latest/actions/perform-a-lookup-enquiry-for-a-mobile-number', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "to": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `to` | string | yes | The mobile number that the service will use. Format with a '+' and country code e.g., +306948530920 (E.164 format). |
| `label` | string | no | A generic label which can be used for tagging the lookup HLR. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "applicationName": "Ava Chen",
      "createdAt": "string",
      "details": {
        "country": {
          "code": "string",
          "isoA3Code": "string",
          "localeName": "Ava Chen",
          "name": "Ava Chen"
        },
        "imsi": "string",
        "mcc": "string",
        "network": {
          "mnc": "string",
          "name": "Ava Chen"
        },
        "ported": true,
        "portedNetwork": {
          "mnc": "string",
          "name": "Ava Chen"
        },
        "roamingNetwork": {
          "country": "string",
          "countryIsoCode": "string",
          "mmc": "string",
          "mnc": "string",
          "network": "string",
          "state": "string"
        }
      },
      "label": "string",
      "lookupId": "string",
      "statusInfo": {
        "description": "string",
        "status": "string",
        "updatedAt": "string"
      },
      "to": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `applicationName` | string |  |
| `createdAt` | string |  |
| `details` | object |  |
| `details.country` | object |  |
| `details.country.code` | string |  |
| `details.country.isoA3Code` | string |  |
| `details.country.localeName` | string |  |
| `details.country.name` | string |  |
| `details.imsi` | string |  |
| `details.mcc` | string |  |
| `details.network` | object |  |
| `details.network.mnc` | string |  |
| `details.network.name` | string |  |
| `details.ported` | boolean |  |
| `details.portedNetwork` | object |  |
| `details.portedNetwork.mnc` | string |  |
| `details.portedNetwork.name` | string |  |
| `details.roamingNetwork` | object |  |
| `details.roamingNetwork.country` | string |  |
| `details.roamingNetwork.countryIsoCode` | string |  |
| `details.roamingNetwork.mmc` | string |  |
| `details.roamingNetwork.mnc` | string |  |
| `details.roamingNetwork.network` | string |  |
| `details.roamingNetwork.state` | string |  |
| `label` | string |  |
| `lookupId` | string |  |
| `statusInfo` | object |  |
| `statusInfo.description` | string |  |
| `statusInfo.status` | string |  |
| `statusInfo.updatedAt` | string |  |
| `to` | string |  |

## Native endpoint

Through the native Routee API, this operation is `POST /lookup` (base URL `https://connect.routee.net`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/perform-a-lookup-enquiry-for-a-mobile-number.md) for the provider-specific parameters and requirements.

