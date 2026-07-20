# Routee: Track a Number Lookup request

Tracks a number lookup request in Routee.

```
GET https://connect.mindcloud.co/v1/universal/routee/latest/actions/track-a-number-lookup-request
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Routee `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/routee/latest/actions/track-a-number-lookup-request?connectionId=$CONNECTION_ID&lookupId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "lookupId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/routee/latest/actions/track-a-number-lookup-request?${params}`, {
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
| `lookupId` | string | yes | The id of the single HLR lookup record |

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
      "price": "string",
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
| `price` | string |  |
| `statusInfo` | object |  |
| `statusInfo.description` | string |  |
| `statusInfo.status` | string |  |
| `statusInfo.updatedAt` | string |  |
| `to` | string |  |

## Native endpoint

Through the native Routee API, this operation is `GET /lookup/:lookupId` (base URL `https://connect.routee.net`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/track-a-number-lookup-request.md) for the provider-specific parameters and requirements.

